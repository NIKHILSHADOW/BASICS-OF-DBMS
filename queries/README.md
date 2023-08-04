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

### Change defination of already defined table
- we need the alter for changing defination

* Add new Column
```
alter table table-name
add column column-name datatype
```

* Modify column 
```

```

### Read from table
```
-- read all rows
select * from table-name

-- read with condition
select * from table-name where id = 1;

-- read selected columns
select column1-name, column2-name from table-name;

-- read selected column values with condition
select column1-name, column2-name from table-name where id =1;
```

### String matching 
```
-- match group of characters (%)
-- select whose column-name-value starts with T
select * from table-name where column-name like 'T%'

-- select whose name ends with T
select * from table-name where name like '%T'

-- select whose name starts with 's' and ends with 'o'
select * from table-name where name like 's%o'

-- matches exactly one character(_)
-- select 5 letter name whose first char is o, third is p and fifth is y
select * from table-name where name like 'o_p_y';

```

### logical operators

```
-- print rows with id =1 or id =3 or id =5
select * from table-name where id=1 or id=3 or id=5;

-- print rows with name = 'pooe' and city='psie'
select * from table-name where name='pooe' and city='psie';

--print rows except whose name='stalin'
select * from table-name where name != 'stalin'

--print rows whose name is not NULL
select * from table-name where name is not NULL;

--print rows whose name is NULL
select * from table-name where name is NULL;

```

