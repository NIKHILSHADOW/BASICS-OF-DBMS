# DBMS

MYSQL, POSTGRES, MONGODB, REDIS, ORACLE, CASSANDRA are DBMS not DB

we use DB like AmazonDB, GoogleDB whose data is stored we generally use that

### DATA
* Data is nothing but information.
* Data is used for Analysis.
s
### DATABASE
* Collection of related data.

### DATABASE MANAGEMENT SYSTEM
* These are softwares that help us manage data.


### FILE SYSTEM 

* Searching element in File is O(n)
* Security is issue(password would help, but protection of partial data is not possible).
* Concurrency is issue
* Data integrity is issue (Redundant(if stored all data at a place), inconsistent(if stored related data together, if changed name at one place, other places it will remain same.))


### REDUNDANT

```
EXAMPLE

RollNo  StudentName age     class   ClassStrength ClassTeacher
1       jill        23      16      87              pok
2       jack        23      15      67              oil
3       joe         23      16      87              pok
4       jop         23      16      87              pok
5       jak         23      15      67              oil
6       joe         23      16      87              pok
...

```


### Inconsistent

I want to add new person of class 17 in student table then, it wont directly add to class table, here if we forgot to add, data will be inconsistent.

or

If we want to change class 16 to 17 then, it wont be directly applied to student table.

or

There might be a class (let's suppose be 18) in students table, which might not be there in class table.

or

lets delete class(16) on class table , but in students table it will not be deleted

These are issues which DBMS handles and file don't

```
EXAMPLE

RollNo  StudentName age     class
1       jill        23      16
2       jack        23      15
3       joe         23      16
4       jop         23      16
5       jak         23      15
6       joe         23      16
...

Class       ClassTeacher    Strength
16          pok             87
15          oil             67

```

### Concurrency

Here in the below table at a point of two people are trying add their names, then we consider last change in file system.

```
StudentName
===========
Vijay
Suresh
Rakesh

insertion of tony and gill at a time, it will consider only one change.

```

* Files are generally used for configurations, logs etc.
* Files are preferred
    * When data is Static(no frequent changes).
    * Small amount of data.
    * While performing only simple operations read and write.


### Random Access vs Sequential Acess
    - Sequential access is searching one by one record.
    - Random access is going directly to that location and searching.

### DATA BASE MANAGEMENT SYSTEM

- Software which help us manage Database.

* Concurrency
* Security
* Integrity
* Efficient
* Views(partial data access)
* Fault tolerance(data losing issues)

Two types of DBMS
    - Relational
    - Non-Relational

### Relational Database Management System


Popular RDBMS
================
* Mysql
* Postgres
* Oracle
* SQLite

### Non-Relational Database Management System

Popular Non-Relational DBMS
============================
* Neo4J (Graph-database)
* Redis (Key-value or map)
* Mongo (Document-based)
* Columnar
* Cassandra
* Time scaled

### Relational model
    - 1960
    - Edgar Codd
    - Turing Award

* Represented in tables.
* Data is stored in rows.

```
Table is a relation.
Tuple is a row.
Attribute is a column.
```

### Tuple
* A Tuple is record or row, is a basic unit of data in rdbms.
* A Tuple represents a single instance of relation or table in database.

### Attributes
* A characteristic of a table.

### Degree
* Number of attributes or Columns

### Cardinality
* Number of rows or tuples.

### Properties of RDMS

* Unique
    - Rows or Tuples should be unique.
    - Attributes or Columns Should be unique.
* Unordered(change in order also represent same)
    - Tuples are unordered.
    - Attributes are unordered.
* Uniform datatype
    - The datatype of an attribute in all tuples is always same in the same table.
* Atomicity
    - It should be atomic in datatype, not in group.
    - As datatype of each attribute is atomic, we can know each tuple size, so we can identify the location of the tuple which we are searching, so we can do random access

** Keys
    - We use keys to uniquely identify tuple.
    - Describe Relationship between relations.

* Super key
    - any set of attributes that uniquely identify a tuple
* Candidate Key
    - Minimal number of attributes that uniquely identify a tuple
* Primary Key
    - One of the Candidate key.

* Composite Key
    - Morethan one column is used to identify the tuple uniquely.

### Data Integrity
    Data Correctness

### ER Diagram
    - In Relation model we use sets.
    - In ER model we use Entity and Relationship
    - Currently we are using ER diagram

### Entity 
    - A real world object that is distinguishable from other objects in real world.

    1. Tangible Entities
        - Entities which has physical presence.
        Ex: Cars, Books, etc.
    2. Non-Tangible Entities
        - Entities which do not have physical prsence.
        Ex: Emailid's, Phone numbers, etc.

### Attribute
    - A Entity property or properties of real world object.


### Data Integrity
    ```
    - Inserting Duplicate rows into table is not allowed.
    - Database don't allow values with invalid datatypes
    - Database didn't allow to delete referenced rows which    causes inconsistency
    ```

    - Entity Integrity :
        - It Ensures rows are unique.
        - PK(unique and not null)
    - Domain Integrity :
        - It Ensures that the table values follow table Structure.
        Ex: Datatype of values under same attribute is to be same, Following NULL rule, Date format should be followed, range of values, size of values should be satisfied.
    - Referential Integrity :
        - It ensures that insertion of Referenced values exist.
        Ex: 

        ```
        Teacher

        |   teacher-name     |   age    |
        --------------------------------
        |   Raveena          |   57     |
        --------------------------------
        |   Olive            |   49     |


        Student

        |   student-name    |   age     |       class       |       teacher-name        |
        --------------------------------------------------------------------------------
        |   Tondon          |   23      |       16          |       Raveena             |
        --------------------------------------------------------------------------------
        |   Ravi            |   21      |       15          |       olive               |


        If we try to insert a value which is not in teacher table it will throw an error
        ```