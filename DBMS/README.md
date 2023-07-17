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

### Properties of RDBMS

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
