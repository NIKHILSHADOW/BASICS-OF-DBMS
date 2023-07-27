# BASIC QUERIES

### Table

* We use CRUD operations 
* C - Create
* R - DESC
* U - Update
* D - Drop


### Row of a table

* C - insert
* R - select
* U - update
* D - delete

### Classification of sql commands

* DDL
* DML
* DCL
* TCL

* DDL(Data Defination Language)
    -   CREATE
    -   ALTER
    -   DROP
    -   TRUNCATE

* DML(Data Manipulation Language)
    -   Insert
    -   Delete
    -   Select
    -   Update

* DCL(Data Control Language)
    -   Grant
    -   Revoke

* TCL(Transaction Control Language)
    -   Rollback
    -   Commit
    -   Begin

* Queries
- Comments in sql can be written using
```
-- Single line Comment (Sql way)
# Single line Comment (Java way)
/*
 Multi-line 
 Comments
*/
```
* Show databases
```
show databases;
```

* Create Database
```
Create Database database-name
```

* Switch to needed database
```
use database-name
```

* drop database
```
drop database database-name
```

* View all tables presnt in current database
```
show tables;
```

* view description of database
```
desc table-name
```

* create table
```
create table table-name
(
    column-name datatype constraints,
    column-name datatype constraints,
    column-name datatype constraints,
    constraints
);

EX:

create table student
(
    id int not null auto_increment,
    first_name varchar(30) not null,
    last_name varchar(30) not null,
    batch_id int,
    primary key(id)
);
```
