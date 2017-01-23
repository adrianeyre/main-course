# Postgres

## Install postgres
```shell
$ brew install postgresql
$ ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents
$ launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
```

## Run postgres
```shell
$ psql
```

## Command
```
\q = Quit
\l = List database

create database "name_of_database";
```
