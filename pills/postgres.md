# Postgres and SQL Help

* [Install Postgres](#Install)
* [Run Postgres](#Run)
* [Postgres Command](#PCommands)
* [Basic SQL Commands](#SQL)

## <a name="Install">Install Postgres</a>
```shell
$ brew install postgresql
$ ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents
$ launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
```

## <a name="Run">Run Postgres</a>
```shell
$ psql
```

## <a name="PCommands">Postgres Command</a>
`\q` = Quit

`\l` = List database

`\d` = List columns on table

`\dt` = List tables in connected database

`\d table_name`= List columns in table

`\c database_name` = Switch to different database

## <a name="SQL">Basic SQL Commands</a>
### Database
`CREATE DATABASE database_name` = Creates a new database

`DROP DATABASE database_name` = Deletes a database

### Tables
```
CREATE table table_name(                # Creates table 'table_name'
id serial PRIMARY KEY,                  # Creates id as Primary Key and uses the serial constraint
column_2_name data_type_for_column_2);  # Creates column 'column_2_name'
```

`DROP table_name;` = Deletes table

`ALTER TABLE table_name ADD column_name datatype;` = Add a column to table

### Select
`SELECT * FROM table WHERE column = 'search';` = Select all from table that equals 'search'

`SELECT DISTINCT column_name(s) FROM table_name;` = Select unique values from table

### Data Manipulation
`INSERT INTO table_name (column1, column2,...) VALUES (value_1, value_2,....);` Inserts data into columns

`UPDATE table_name SET column_name_1 = new_value_1 WHERE column_name_1 = 'something';` Updates data into columns

`DELETE FROM table_name WHERE column_name = some_value;` = Delete data from table
