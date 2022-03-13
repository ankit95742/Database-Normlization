# Database-Normlization

## What is the Database Normlization?

Normalization is a darabase technique that reduces data redundacy and eliminates undesiable characteristics like insertion, update and deletion anomalies. Normalization rules divides larger table into smaller tables and links them using relationships.

## First Normal Form (1 NF)

Rules : 1. Each table cell should contain a single value.
        2. Each record needs to be unique.
        
Example : relation STUDENT in table 1 is not in 1NF because of multi-valued attribute STUD_PHONE. Its decomposition into 1NF has been shown in table 2.

![image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20210115105301/1239.png)

Primary Key : A Primary is a single column value used to identify a database record uniquely. A primary key cannot be NULL. A primary key value must be unique. The primary key values should rarely be chnaged. The primary key must be given a vlaue when a new record is inserted.

## Second Normal Form (2 NF)

Rules : 1. Be in 1NF
        2. Single Column Primary key that does not functionally dependant on any subset of candidate key relation.
        
![image](https://www.guru99.com/images/Table2.png)

To convert the above table to 2NF. We have to divied our tabel into two table. Table 1 and Table 2. Table 1 contains member information. Table 2 contains information on movies rented.

![image](https://www.guru99.com/images/Table1.png)

We have introduction a new columns call Membership_id which is the primary key for table 1. Records can be uniquely identified in Tabte 1 using membership id.

Foreign key : Foregin key references the primary key of another Table! It helps connect your Table.A foreign key can have a different name from its primary key. It ensures rows in one table have corresponding rows in another.
Unlike the primary key, they do not have to be unique. Most often they aren't.

## Third Normal Form (3NF) :

Rules : 1. A Table is already in 2NF.
        2. Non-Primary key columns shouldn't depend on the other non-primary key columns.
        3. There is no transitive functional dependency.

Transitive dependency – If A->B and B->C are two FDs then A->C is called transitive dependency.

![image](https://www.guru99.com/images/2NFTable1.png)
![image](https://www.guru99.com/images/2NFTable2.png)
![image](https://www.guru99.com/images/2NFTable3.png)

There are no transitive functional dependencies, and hence our table is in 3NF.

## Fourth Normal Form (4NF)

If no database table instance contains two or more, independent and multivalued data describing the relevant entity, then it is in 4th Normal Form.

## Fifth Normal Form (5NF)

A table is in 5th Normal Form only if it is in 4NF and it cannot be decomposed into any number of smaller tables without loss of data.
