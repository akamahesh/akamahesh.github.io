---
layout: post
title: The Sequel to SQL
date: 2017-12-12 00:00:00 +0300
description: Advance SQL # Add post description (optional)
img: sql-sequel.png # Add image post (optional)
tags: [SQL, database] # add tag
---

# The Sequel to SQL
Level 1- section 1
### Common Aggregate Functions
Finding the Number of Rows

Q. How do we find the total number of rows in the Movies table?

```SQL
SELECT count(*)
FROM Movies;
```

Total number of rows that match our search
```SQL
SELECT count(column_name)
FROM table_name;
```

Returns the added sum of values for a group of rows.
```SQL
SELECT sum(colomn_name)
FROM table_name;
```

Returns the largest value in a group of rows.
```SQL
SELECT max(column_name)
FROM table_name;
```

Returns the smallest value in a group of rows

```SQL
SELECT min(column_name)
FROM table_name;
```

```SQL
SELECT avg(column_name)
FROM table_name;
```


**Aggregate Functions within SQL Clauses**

```SQL
SELECT genre,sum(cost)
FROM movies
GROUP BY genre;
```

```SQL
SELECT colomn_name, aggregate_function(colomn_name)
FROM table_name
GROUP BY column_name;
```

```SQL
SELECT genre, sum(cost)
FROM Movies
GROUP BY genre
HAVING COUNT(*)>1;
```

The HAVING clause restricts the groups of rows to only those who meet the specified condition.

```SQL
SELECT column_name, aggregate_function(column_name)
FROM table_name
Where colomn_name
HAVING aggregate_function(column_name) operator value;
```

## LEVEL 2 - Section 1
### IDENtifying Constraints

(column constraints)
```SQL
CREATE TABLE Promotions
(
  id int,
  name varchar(50) NOT NULL UNIQUE,
  category varchar(15)
);
```
Why use Constraints?
> Prevent Null values
> Ensure column values are unique
> Provide additional validations


manually sign Constraints name like this
(table Constraints)
```SQL
CREATE TABLE Promotions
(
  id int,
  name varchar(50) NOT NULL,
  category varchar(15),
  CONSTRAINT unique_name UNIQUE(name)
);
```

### Primary key
can be defined only in once in a table
```SQL
CREATE TABLE Promotions
(
  id int PRIMARY KEY,
  name varchar(50),
  category varchar(15)
);
```

## LEVEL 2- SECTION 2
### Value Constraints

Foreigh KEY

movie_id is a foreign key.  
A foreign key is a column in 1 table that references the primary key column of another table.

 **Creating a FOREIGN KEY constraint**  
The REFERENCES keyword can be used to make a FOREIGN KEY constraint.  
```SQL
CREATE TABLE Movies
(
   id int PRIMARY KEY,
   title varchar(20) NOT NULL UNIQUE
);
```

 ```SQL
CREATE TABLE Promotions
(
  id int PRIMARY KEY,
  movie_id int REFERENCES movies(id),
  name varchar(50),
  category varchar(15)
);
 ```

or we can just use REFERENCES movies instead  
or we can just use
```SQL
CREATE TABLE Promotions
(
 id int PRIMARY KEY,
 movie_id int ,
 name varchar(50),
 category varchar(15),
 FOREIGN KEY (movie_id) REFERENCES movies
);
```
#### Orphan Records
Orphan records are child records with a foreign key to a parent record that has been deleted.

>The FOREIGN KEY constraint help to prevent orphan records

** CHECK Constraint**

```SQL
CREATE TABLE Movies
(
  id int PRIMARY KEY,
  title varchar(20) NOT NULL UNIQUE,
  genre varchar(100),
  duration int CHECK (duration > 0)
);
```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
