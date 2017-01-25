# DataMapper Help

* [DataMapper Command] (#DCommands)
* [Using DataMapper] (#use)
* [Relationships] (#rel)

## <a name="DCommands">DataMapper Commands</a>
`Class_Name.create(Method_Name: "Data")` = Inserts data into database

`Class_Name.first_or_create(Method_Name: "Data")` = Insert data if it doesnt already exist in the database

`Class_Name.update(Method_Name: "Data")` = Updates database entry

```
student = Class_Name.first(Method_Name: 'Data')  # Deletes result of student
student.destroy
```

## <a name="rel">Relationships</a>

`has n` =	has_many

`has 1` =	has_one

`belongs_to` = 	belongs_to

`has n, :things, through: Resource` = has_and_belongs_to_many

`has n, :things, through: :model` =	has_many :association, :through => Model

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
