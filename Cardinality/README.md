### Cardinality
    It is defined as number of times an entity of an entity set participates in a relationship set.

Types of Cardinality 
    1. One-to-One.
    2. One-to-many.
    3. Many-to-one.
    4. Many-to-Many.

1. One-to-one :
    An entity in a set relates exactly one occurrence of another entity in another set.

    Ex : If there is a space, where each husband has only one wife and vice versa.
    Then 
    if we represent Husband in one entity table, and wife data in another entity table,
    then the relation between them is 1:1.

2. One-to-many
    An Entity in a set relates more than one occurrence of another entity in another set.

    Ex: If there is a space, where students and batches are entities, each student can be assigned to one batch, but each batch contains more than one students.
    student : batch = n:1

3. Many-to-one
    many Entities in a set relates to one entity in another set.
    
    Ex: If there is a space, where there are two entities House and Rooms, each house contains more than one rooms, but each room is part of one house.

    Here Cardinality of house to room is 1:n

4. Many-to-many
    Each entity of a set contain more than one entity of another set, vice versa.

    Ex: If there is a space, where there two entities students and courses, each student can be assigned to more than one course, and each course can be assigned to more than one student.

    Student : course is 
    1 : m
    n : 1
    => n : m
    