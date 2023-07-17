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