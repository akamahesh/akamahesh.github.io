---
layout: post
title: Hackerrank - SQL Notes
date: 2017-12-18 00:00:00 +0500
description: SQL QUERY Notes # Add post description (optional)
img: hackerearth.jpg # Add image post (optional)
tags: [SQL] # add tag
---

# Hackerrank : SQL Notes  
https://www.w3resource.com/mysql-exercises/
https://dev.mysql.com/

> Returns the difference between city and distinct city in STATION  table

```SQL
SELECT (COUNT(CITY)-COUNT(DISTINCT(CITY)))
FROM STATION;
```
>Query the two cities in STATION with the shortest and longest CITY names, as well as their respective length .

```SQL
SELECT CITY,LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) ASC ,
CITY LIMIT 1;

SELECT CITY, LENGTH(CITY)
FROM STATION
ORDER BY LENGTH(CITY) DESC,
CITY LIMIT 1;

```

> Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

```SQL
SELECT DISTINCT CITY
FROM STATION
WHERE CITY REGEXP "^[aeiou].*";
```
>Query the list of CITY names ending with vowels (a,e,i,o,u) from STATION .

```SQL
SELECT DISTINCT CITY
FROM STATION
WHERE CITY LIKE '%A'
OR CITY LIKE '%E'
OR CITY LIKE '%I'
OR CITY LIKE '%O'
OR CITY LIKE '%U';
```

>Query the list of CITY names NOT ending with vowels (a,e,i,o,u) from STATION .

```SQL
SELECT DISTINCT CITY
FROM STATION
WHERE CITY REGEXP '[^aeiou]$'
```



>Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters.

```SQL
SELECT DISTINCT CITY
FROM STATION
WHERE CITY REGEXP '^[aeiou].*[aeiou]$';
```

>Query the Name of any student in STUDENTS who scored higher than  Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

```SQL
SELECT NAME
FROM STUDENTS
WHERE MARKS > 75
ORDER BY RIGHT(NAME, 3), ID ASC;
```
>Write a query identifying the type of each record in the TRIANGLES table using its three side lengths.

```SQL
SELECT CASE
WHEN A + B > C THEN CASE WHEN A = B AND B = C THEN 'Equilateral' WHEN A = B OR B = C OR A = C THEN 'Isosceles' WHEN A != B OR B != C OR A != C THEN 'Scalene' END
ELSE 'Not A Triangle' END FROM TRIANGLES;
```
