# Heroku Help


## Setting up a new Heroku Applicaion
```shell
$ heroku login

$ heroku git:remote -a name_of_application

$ git push heroku branch_name:master
```

## Create a postgres database on Heroku
```shell
$ heroku addons:create heroku-postgresql:hobby-dev
```
Use `ENV['DATABASE_URL']` in your app to retrieve database name
