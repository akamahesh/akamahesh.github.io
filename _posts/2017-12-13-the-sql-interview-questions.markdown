---
layout: post
title: MySQL Interview Questions
date: '2017-12-16 00:00:00 +0300'
description: Advance SQL
img: i-rest.jpg
tags:
  - SQL
  - database
---

# MySQL Interview Questions

> How is get Structure of table in MYSQL ?

```SQL
DESC TABLENAME
```
> What is MySQL?

MySQL is a multithreded, multi-user SQL Database manangement system which has more than 11 million installations. This is the world's second most popular and widely used open source database. MySQL is writting in C and C++ and its SQL parser is written in yacc.

>What are the technical specification of MySQL?

- Flexible Structure
- High performance
- Manageable and easy to use
- Replication and high availability
- Security and storage management

> What are the different tables present in MySQL?

Tables that remain present by default. MyISAM is the default database engine used in MySQL.
1. MyISAM
2. Heap
3. Merge
4. INNO DB
5. ISAM

> How many Triggers are possible in MYSQL?

A trigger us a set of codes that executes in response to some events. There are only six Triggers allowed to use in MYSQL database.
1. Before insert
2. After insert
3. Before update
4. after update
5. before delete
6. after delete


> What are the data types available in MYSQL?  

INT,VARCHAR, DOUBLE, FLOAT etc.
1. Numeric Datatype
2. Date and Time Datatype
3. String Datatype

>How man types of JOIN are supported by MySQL?

All type of join supports in mysql are: INNER, FULL, LEFT, RIGHT, UNION .

>Routeines and Stored Procedure ?

Yet to get Answered

>Command to show the current version of MYSQL

SELECT VERSION();

>What is the difference between NOW() and CURRENT_DATE()?

 Now() command shows current year, month, date with hours, minutes and seconds. CURRENT_DATE() show cureent year , month, and date only.

> How to display Nth highest salary from a table in MYSQL query?

```SQL
SELECT DISTINCT(salary)
FROM employee
ORDER BY salary DESC limit n-1,1;
```

>Query to display top 20 rows?

```SQL
SELECT *
FROM TABLENAME
LIMIT 0,20;
```

>What is the usage of regular expressions in MySQL?

```SQL
Select employee_name  
From employee  
Where employee_name REGEXP '1000'  
Order by employee_name  
```

>What do DDL, DML, and DCL stand for?

DDL data defination language CREATE TABLE
DML data manipulation language SELECT INSERT
DCL data control language GRANT REVOKE

>What are the different types of strings in Database columns in MySQL?

Different types of strings that can be used for database columns are SET, BLOB, VARCHAR, TEX, ENUM, and CHAR.

>What are the different types of tables in MySQL?

MyISAM is the default table that is based on the sequential access method.

1. HEAP is the table that is used for fast data access but data will be lost if the table or system crashes.
2. InoDB is the table that supports transactions using the COMMIT and ROLL BACK commands.
3. BDB can support transactions similar to InoDB but the execution is slower.

>What is the difference between LIKE and REGEXP operators in MySQL?

 LIKE is denoted using the % sign. For example:SELECT * FROM user WHERE user name LIKE “%NAME”.• On the other hand the use of REGEXP is as follows:SELECT * FROM user WHERE username REGEXP “^NAME”;

> How can one take incremental backup in MySQL?

User can take incremental backup in MySQL using percona xtrabackup.

>Properties of the Relational tables?

Relational tables have six Properties:
1. Values are atomic.
2. Column values are the same kind.
3. Each row is unique.
4. The sequence of columns is insignificant.
5. The sequence of rows is insignificant.
6. Each column must have a unique name.

> What is Normalization?

Database Normalization is a data design and organiztion process applied to data structures based on rules that help building relational databases. In relational database design, the process of organizing data to minimize redundancy is called normalization.

> What are different normalization forms?

1. 1NF: Eliminate Repeating Groups Make a separate table for each set of related attributes, and give each table a primary key. Each field contains at most one value from its attribute domain.
2. 2NF: Eliminate Redundant Data If an attribute depends on only part of a multi-valued key, remove it to a separate table.
3. 3NF: Eliminate Columns Not Dependent On Key If attributes do not contribute to a description of the key, remove them to a separate table. All attributes must be directly dependent on the primary key.
4. BCNF: Boyce-Codd Normal Form If there are non-trivial dependencies between candidate key attributes, separate them out into distinct tables.
5. 4NF: Isolate Independent Multiple Relationships No table may contain two or more 1:n or n:m relationships that are not directly related.
6. 5NF: Isolate Semantically Related Multiple Relationships There may be practical constrains on information that justify separating logically related many-to-many relationships.
7. ONF: Optimal Normal Form A model limited to only simple (elemental) facts, as expressed in Object Role Model notation.
8. DKNF: Domain-Key Normal Form A model free from all modification anomalies is said to be in DKNF.  
Remember, these normalization guidelines are cumulative. For a database to be in 3NF, it must first fulfill all the criteria of a 2NF and 1NF database.

> What is View?

A simple view can be thought of as a subset of a table. It can be used for retrieving data, as well as updating or deleting rows. Rows updated or deleted in the view are updated or deleted in the table the view was created with. It should also be noted that as data in the original table changes, so does data in the view, as views are the way to look at part of the original table. The results of using a view are not permanently stored in the database. The data accessed through a view is actually constructed using standard T-SQL select command and can come from one to many different base tables or even other views.


>What are different Types of Join?

1. **Cross Join** A cross join that does not have a WHERE clause produces the Cartesian product of the tables involved in the join. The size of a Cartesian product result set is the number of rows in the first table multiplied by the number of rows in the second table. The common example is when company wants to combine each product with a pricing table to analyze each product at each price.
2. **Inner Join** A join that displays only the rows that have a match in both joined tables is known as inner Join. This is the default type of join in the Query and View Designer.
3. **Outer Join** A join that includes rows even if they do not have related rows in the joined table is an Outer Join. You can create three different outer join to specify the unmatched rows to be included:
  -  **Left Outer Join**: In Left Outer Join all rows in the first-named table i.e. "left" table, which appears leftmost in the JOIN clause are included. Unmatched rows in the right table do not appear.
  - **Right Outer Join**: In Right Outer Join all rows in the second-named table i.e. "right" table, which appears rightmost in the JOIN clause are included. Unmatched rows in the left table are not included.
  - **Full Outer Join**: In Full Outer Join all rows in all joined tables are included, whether they are matched or not.
4. **Self Join** This is a particular case when one table joins to itself, with one or two aliases to avoid confusion. A self join can be of any type, as long as the joined tables are the same. A self join is rather unique in that it involves a relationship with only one table. The common example is when company has a hierarchal reporting structure whereby one member of staff reports to another. Self Join can be Outer Join or Inner Join.

>What is Data Warehousing?

Subject-oriented, meaning that the data in the database is organized so that all the data elements relating to the same real-world event or object are linked together;
Time-variant, meaning that the changes to the data in the database are tracked and recorded so that reports can be produced showing changes over time;
Non-volatile, meaning that data in the database is never over-written or deleted, once committed, the data is static, read-only, but retained for future reporting.
Integrated, meaning that the database contains data from most or all of an organization's operational applications, and that this data is made consistent.

<<<<<<< HEAD
>Difference between HAVING and WHERE

HAVING specifies a search conditon for a group or an aggregate function used in SELECT statement.  
HAVING can be used only with SELECT statement.   
HAVING is typically used in a GROUP BY clause. When GROUP BY is not used. HAVING behaves like a WHERE clause.  

Example of HAVING and WHERE in one query:  
```SQL
SELECT titles.pub_id, AVG(titles.price)
FROM titles INNER JOIN publishers
ON titles.pub_id = publishers.pub_id
WHERE publishers.state = 'CA'
GROUP BY titles.pub_id
HAVING AVG(titles.price) > 10
```

>SQL RIGHT() function

Extract a substring from a string (starting from right):

```SQL
SELECT RIGHT('SQL HIRE ME',3) AS EXTRACTSTRING
FROM CUSTOMERS;
```
store last three char to EXTRACTSTRING;

>
=======
>What is PL/SQL?  

- PL/SQL is the language we use to write reusable Oracle code.
- PL in PL/SQL stands for procedural language.
- In Oracle you can store PL/SQL code in stored procedures, functions, and packages (packages consist of a specification and body).

>MySQL - Data types

**Numeric Data Types**
1. INT - 11 digits
2. TINYINT -
3. SMALLINT -
4. MEDIUMINT -
5. BIGINT -
6. FLOAT(M,D) -
7. DOUBLE(M,D) -
8. DECIMAL(M,D) -

**Data and Time Types**
1. Date
2. DATETIME
3. TIMESTAMP
4. TIME
5. YEAR(M)

**String Types**
1. CHAR(M)
2. VARCHAR(M)
3. BLOB OR TEXT
4. TINYBLOB OR TINYTEXT
5. MEDIUMBLOB OR MEDIUMTEXT
6. LONGBLOB OR LONGTEXT
7. ENUM


>Creating deleting altering databases and Tables
>Connection with databases
>Primary keys, index keys and foreign keys
>How you start designing tables as per the requirement
>Selection Query
>Optimizing the queries with left and right joins
>Aggregating functions
>Selecting the unique Rows
>avoiding the duplicate Rows
>Search in MySQL tables
>technical features and General knowledge topics about MYSQL.
>>>>>>> 0bbf81fea6cbdf9efb90ab1291cd753b1382870b
