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
`\q` = Quit

`\l` = List database

`\d` = List columns on table

`\dt` = List tables in connected database

`\d table_name`= List columns in table

`\c database_name` = Switch to different database

`create database "name_of_database";` = Creates a database

## Basic SQL Commands
### Tables
```
CREATE table "table_name"(                   # Creates table 'table_name'
id serial PRIMARY KEY,                       # Creates id as Primary Key and uses the serial (increment +1) constraint
"column_2" "data_type_for_column_1");        # Creates column 'column_1'
```

`DROP table_name` = Deletes table

### Search Data
`SELECT * FROM table WHERE column = 'search';`

### Data Manipulation
`INSERT INTO table_name (column1, column2,...) VALUES (value_1, value_2,....)` Inserts data into columns

`UPDATE table_name SET column_name_1 = new_value_1 WHERE column_name_1 = 'something'` Updates data into columns
