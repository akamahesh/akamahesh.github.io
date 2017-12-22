---
layout: post
title: Hackerrank - SQL Notes
date: 2017-12-20 00:00:00 +0500
description: SQL QUERY Notes # Add post description (optional)
img: how-to-start.jpg # Add image post (optional)
tags: [Java] # add tag
---

# Hackerrank : SQL Notes  

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


```SQL
```


```SQL
```
