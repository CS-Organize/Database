# PostgreSQL

## Installation

```bash
brew install postgresql
brew services start postgresql
# brew services stop postgresql
```

## Usage

```bash
psql postgres
psql -U <user_name> -d <db_name>
```

## Commands

### General

```sql
\q -- Quit
\? -- Help
```

### DB Management

```sql
CREATE DATABASE <db_name>; -- Create Database
\l -- List Databases
DROP DATABASE <db_name>; -- Drop Database
\c <db_name>; -- Connect to Database
```

### User Management

```sql
CREATE USER <user_name> WITH PASSWORD '<password>'; -- Create User
\du -- Describe Users
GRANT ALL PRIVILEGES ON DATABASE <db_name> TO <user_name>; -- Grant Privileges
ALTER USER <user_name> WITH SUPERUSER; -- Change User Role
ALTER USER <user_name> WITH PASSWORD '<password>'; -- Change User Password
ALTER USER <user_name> WITH LOGIN; -- Change User Login
ALTER USER <user_name> WITH NOLOGIN; -- Change User No Login
DROP USER <user_name>; -- Drop User
```

### Table Management

```sql
CREATE TABLE <table_name> (
    <column_name> <data_type> <constraint>,
    ...
); -- Create Table
\dt -- Describe Tables
INSERT INTO <table_name> (<column_name>, ...) VALUES (<value>, ...); -- Insert Data
SELECT * FROM <table_name>; -- Select Data
UPDATE <table_name> SET <column_name> = <value> WHERE <condition>; -- Update Data
DROP TABLE <table_name>; -- Drop Table
```
