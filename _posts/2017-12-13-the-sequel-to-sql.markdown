---
layout: post
title: The Sequel to SQL
date: '2017-12-12 00:00:00 +0300'
description: Advance SQL
img: sql-sequel.png
tags:
  - SQL
  - database
---

# The Sequel to SQL

Level 1- section 1

## Common Aggregate Functions

Finding the Number of Rows

Q. How do we find the total number of rows in the Movies table?

```sql
SELECT count(*)
FROM Movies;
```

Total number of rows that match our search

```sql
SELECT count(column_name)
FROM table_name;
```

Returns the added sum of values for a group of rows.

```sql
SELECT sum(colomn_name)
FROM table_name;
```

Returns the largest value in a group of rows.

```sql
SELECT max(column_name)
FROM table_name;
```

Returns the smallest value in a group of rows

```sql
SELECT min(column_name)
FROM table_name;
```

```sql
SELECT avg(column_name)
FROM table_name;
```

**Aggregate Functions within SQL Clauses**

```sql
SELECT genre,sum(cost)
FROM movies
GROUP BY genre;
```

```sql
SELECT colomn_name, aggregate_function(colomn_name)
FROM table_name
GROUP BY column_name;
```

```sql
SELECT genre, sum(cost)
FROM Movies
GROUP BY genre
HAVING COUNT(*)>1;
```

The HAVING clause restricts the groups of rows to only those who meet the specified condition.

```sql
SELECT column_name, aggregate_function(column_name)
FROM table_name
Where colomn_name
HAVING aggregate_function(column_name) operator value;
```

## LEVEL 2 - Section 1

### IDENtifying Constraints

(column constraints)

```sql
CREATE TABLE Promotions
(
  id int,
  name varchar(50) NOT NULL UNIQUE,
  category varchar(15)
);
```

Why use Constraints?

> Prevent Null values Ensure column values are unique Provide additional validations

manually sign Constraints name like this (table Constraints)

```sql
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

```sql
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

movie_id is a foreign key.<br>
A foreign key is a column in 1 table that references the primary key column of another table.

**Creating a FOREIGN KEY constraint**<br>
The REFERENCES keyword can be used to make a FOREIGN KEY constraint.

```sql
CREATE TABLE Movies
(
   id int PRIMARY KEY,
   title varchar(20) NOT NULL UNIQUE
);
```

```sql
CREATE TABLE Promotions
(
  id int PRIMARY KEY,
  movie_id int REFERENCES movies(id),
  name varchar(50),
  category varchar(15)
);
```

or we can just use REFERENCES movies instead<br>
or we can just use

```sql
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

> The FOREIGN KEY constraint help to prevent orphan records

**CHECK Constraint**

```sql
CREATE TABLE Movies
(
  id int PRIMARY KEY,
  title varchar(20) NOT NULL UNIQUE,
  genre varchar(100),
  duration int CHECK (duration > 0)
);
```

First Header | Second Header
------------ | -------------
Content Cell | Content Cell
Content Cell | Content Cell
