# Ruby on Rails

## Installation
```
$ gem install rails
```

# Rspec installation for Rails
`$ bin/rails generate rspec:install`

# Rake files
`$ bin/rake db:create` = Creates database<br>
`$ bin/rake db:purge` = Deletes database<br>
`$ bin/rake db:purge RAILS_ENV=test` = Deletes test database<br>
`$ bin/rake db:migrate` = Updates database schema<br>
`$ bin/rake db:purge RAILS_ENV=test` = Updates test database schema<br>
`$ bin/rake routes` = Display RESTful routes

# Create New Controller
`$ bin/rails g controller <name>` where name is the name of the controller

# Create New Model
`$ bin/rails g model <name> <column name>:<type>` where name is the name of the model
