# DBMS

MYSQL, POSTGRES, MONGODB, REDIS, ORACLE, CASSANDRA are DBMS not DB

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