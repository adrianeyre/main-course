# DataMapper Help

* [DataMapper Command] (#DCommands)
* [Using DataMapper] (#use)

## <a name="DCommands">DataMapper Commands</a>
`Class_Name.create(Method_Name: "Data")` = Inserts data into database

```
student = Class_Name.first(Method_Name: 'Data')  # Deletes result of student
student.destroy
```
## <a name="use">Using DataMapper</a>
```ruby
require 'dm-migrations'
require 'data_mapper'
require 'dm-postgres-adapter'

DataMapper::Logger.new($stdout, :debug)  # Sets the debugging to the output

DataMapper.setup(:default, "postgres://localhost/DATABASE_NAME")  # Sets database connection

class Student
  # Give the class some database-interaction superpowers
  include DataMapper::Resource

  # Tell the class which columns exist in the student table
  property :id,     Serial
  property :name,   String
end

DataMapper.finalize

DataMapper.auto_upgrade!
```
