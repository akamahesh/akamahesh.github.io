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


```SQL
```


```SQL
```


```SQL
```


```SQL
```
