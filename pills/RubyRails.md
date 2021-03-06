# Ruby on Rails

## Installation
```
$ gem install rails
```

# Rspec installation for Rails
`$ bin/rails generate rspec:install`

# Run Rails Server
` bin/rails server`

# Rake files
`$ bin/rake db:create` = Creates database

`$ bin/rake db:purge` = Deletes database

`$ bin/rake db:purge RAILS_ENV=test` = Deletes test database

`$ bin/rake db:migrate` = Updates database schema

`$ bin/rake db:purge RAILS_ENV=test` = Updates test database schema

`$ bin/rake routes` = Display RESTful routes

# Create New Controller
`$ bin/rails g controller <name>` where name is the name of the controller

# Create New Model
`$ bin/rails g model <name> <column name>:<type>` where name is the name of the model

# Permit params
`params.require(:<table>).permit(:<column>)`

# Create database dependancy
```ruby
class Main_Table < ActiveRecord::Base
  has_many :second_table, dependent: :destroy
end
```

# Database validation
`validates :<column>, length: { minimum: 3 }, uniqueness: true` = validates column length to a minimum of 3

`validates :<column>, inclusion: (1..5)` = validates range

# Devise - User setup
Add the `gem 'devise'` gem in the `gemfile`
```shell
$ bin/rails g devise:install    # Installed devise
$ bin/rails g devise User       # Creates user model
$ rake db:migrate               # Updates database schema
```
