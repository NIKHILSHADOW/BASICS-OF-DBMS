# NORMALIZATION

## DATABASE DESIGN
* The overall design of the database is called the database schema.

* Database has several schemas based on the level of abstraction.
    * Physical Schema
    * Logical Schema
    * View Schema

* The Relationship schema has several undesirable problems.

#### 1. Redundancy :
    * The aim of database design is to to reduce the redundancy.
```
StudentID   |   Name    |   CourseID    |   CourseName  |
------------|-----------|---------------|---------------|
    1       |   Ajay    |   536         |   DBMS        |
    2       |   Suresh  |   536         |   DBMS        |
    3       |   Rajesh  |   536         |   DBMS        |
    4       |   Kiran   |   7437        |   OS          |
    5       |   Ozio    |   8483        |   MS Excel    |
    6       |   Yakir   |   7437        |   OS          |

    Here We can see repetition of Course name is happening, which is redundant data.

```

#### 2.  Update Anomalies : 
    * Multiple Copies of same data, may lead to update anomaly or inconsistency.

```
StudentID   |   Name    |   PhoneNumber |   Courseid    |
------------|-----------|---------------|---------------|
1           |   Ajay    |   123         |   ui          |
1           |   Ajay    |   123         |   ux          |
1           |   Ajay    |   123         |   os          |
2           |   Avi     |   826         |   dbms        |

    If we try to update Ajay's phone number to 674 then it will lead to inconsistent data, if not updated in all rows where Ajay data is present.
```

#### 3.  Insertion Anomalies :
    *   If there is a data, where we cant enter one data without having other data(primary key data).

```
StudentId   |   Name    |   MentorID   |   MentorName   |
------------|-----------|--------------|----------------|
1           |   Jill    |   47         |    iqmaster    |
2           |   Gill    |   83         |    genius      |

Here I will have problem, when i want to add new teacher, because StudentId is primary key we cat enter the data of teacher unless we add the data of teacher.
```

#### 4.  Deletion Anomalies :
    * If there is data dependent on other data, if we delete data of one type, dependent data also gets deleted.

```
    StudentID   |   S_Name     |   CourseId    |   C_Fee    |
    ----------  |  ----------  |  -----------  |  --------  |
    1           |   Jill       |    4          |    26620   |
    2           |   jiah       |    2          |    77337   |
    3           |   usi        |    3          |    73273   |
    4           |   ieye       |    1          |    37373   |

    Here Student with Id = 4, wants to Unsubscribe for the course then the information of the course Id = 1 , will be lost.
```

##  Functional Dependency

### 1. Trivial Dependency :
        - A functional dependency of the form X->Y is trivial if Y ⊆ X.
### 2.  Full Functional Dependency :
        - A FD X->Y is a full functional dependency if removal of any Attribute A from X means that the dependency doesnot hold true.
### 3.  Partial Dependency :
        - A FD X->Y is a partial dependency if some attribute A ∈ X can be removed from X and then the dependency still hold true.
### 4.  Transitive Dependency   :
        - A FD P->Q and Q->R holds then P->R is transitive dependency.
### 5.  Multi-valued Dependency :
        **** to be added        ****

###  PRIME ATTRIBUTE :
    -   An attribute of relational schema R is called a prime attribue of R if it is a member of some candidate key of R.


## NORMALIZATION
    - The goal of a relational database design is to generate a set of relational schemas that allows us to store information without any redundant data. It also allows us to retrieve easily and more efficiently.

    - We follow 

