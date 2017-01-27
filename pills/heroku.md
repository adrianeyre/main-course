# Heroku Help


## Setting up a new Heroku Applicaion
```shell
$ heroku login

$ heroku git:remote -a name_of_application

$ git push heroku branch_name:master -f
```

## Create a postgres database on Heroku
```shell
$ heroku addons:create heroku-postgresql:hobby-dev
```
Use `ENV['DATABASE_URL']` in your app to retrieve database name

## Upgrade database using a Rakefile

### Rakefile
```ruby
require 'data_mapper'

namespace :db do
  desc "Non destructive upgrade"
  task :auto_upgrade do
    DataMapper.auto_upgrade!
    puts "Auto-upgrade complete (no data loss)"
  end


  desc "Destructive upgrade"
  task :auto_migrate do
    DataMapper.auto_migrate!
    puts "Auto-migrate complete (data was lost)"
  end
end
```

### Command to run Rakefile on Heroku database
```shell
$ heroku run rake db:auto_upgrade
```
