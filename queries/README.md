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
alter table table-name
modify column-name new-data-type
```

* Rename column
```
alter table table-name
change old-column-name new-column-name 
```

* Deleting column 

```
alter table table-name 
drop column-name
```

* add primary key

```
ALTER TABLE table-name
ADD CONSTRAINT pk_student_id PRIMARY KEY (column-name);
```
* Add foreign 


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

* match group of characters (%)
* select whose column-name-value starts with T
``` 
select * from table-name where column-name like 'T%'
```

* select whose name ends with T
```
select * from table-name where name like '%T'
```

-- select whose name starts with 's' and ends with 'o'
```
select * from table-name where name like 's%o'
```

* matches exactly one character(_)
* select 5 letter name whose first char is o, third is p and fifth is y
```
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

-- not equal in sql also represented using '<>'
select * from table-name where name <> 'stalin'

--print rows whose name is not NULL
select * from table-name where name is not NULL;

--print rows whose name is NULL
select * from table-name where name is NULL;

```

### reduce code by using 'in' in place of or

```
// select rows with id =1 or id=2 or id=4
select * from table-name where id in (1,2,4);

// select rows whose id not equal 1 and 2 and 3
select * from table-name where not in (1,2,3);
```

### print in order 
```
-- select rows in the increasing order of id
select * from table-name order by id;

-- select rows in the decreasing order of id
select * from table-name order by id desc;


```

### Select only first n rows
```
-- select first 5 rows
select * from table-name limit 5;

-- select top 5 rows in order of rank
select * from table-name order by rank limit 5;

-- select top 5 rows in order by marks
select * from table-name order by marks desc limit 5;

```

### Select x rows from 3rd row
```
-- select 5 rows from 3rd row
select * from table limit 5 offset 2;

-- select 2nd row
select * from table-name limit 1 offset 1;
```

### Update table

*    update table rows

```
update table-name set column-name = 'value' 
```

* update table rows with condition

```
update table-name set column-name='value' where id=1;

```


### Delete rows

```
-- delete all rows
delete from table-name

-- delete rows with condition 
delete from table-name where name='iifif';
```

### Truncate table

```
-- Deletes all rows of table at a time unlike the delete which deletes one by one 
-- Truncate deletes only table data, not table structure.

truncate table table-name
```

### Drop 
```
-- drop database deletes all tables and deletes database, all structures will be deleted

-- drop database
-------------------
drop database database-name


-- drop table
-------------------
-- unlike truncate drop table deletes data as well as table structures.
drop table table-name

```

# Grant and Revoke
----------------------
```
-- Grant gives permission to user to interact with table , views etc.

grant select on table-name to user-name


-- Revoke takes back the permission given by grant

revoke insert, update 

```