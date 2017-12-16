---
layout: post
title: The Sequel to SQL Level-4
date: '2017-12-12 00:00:00 +0300'
description: Advance SQL
img: sql-sequel.png
tags:
  - SQL
  - database
---

# The Sequel to SQL

Level 4 - Section 1

## Inner Joins

**Fetching Data From Multiple Tables:**  
```SQL
SELECT review, movie_id
FROM Reviews;
```
Fetches all the reviews  
```SQL
SELECT title
FROM Movies
WHERE id IN (1,3,4);
```
Fetches all the associated movie titles
- Now How we can return this data using 1 query instead of 2.
- Two tables can be joined by the primary key and a foreign key.  
- Using the INNER JOIN to create this query, we can show where both tables have matching values.  

```SQL
SELECT  *
FROM Movies
INNER JOIN Reviews
On Movies.id=Reviews.movie_id  
```
- what if we only wanted the movie title and review text to be returned?  
```SQL
SELECt Movies.title, Reviews.review
FROM Movies
INNER JOIN Reviews
ON Movies.id = Reviews.movie_id
```
- How do we find genres of Peter Pan?  
```SQL
SELECT Movies.title, Genres.name
FROM Movies
INNER JOIN Movies_Genres
ON Movies.id = Movies_Genres.movie_id
INNER JOIN Genres
ON Movies_Genres.genre_id = Genres.id
WHERE Movies.title = "Peter Pan";
```
## Level 4 - Section 2 Aliases
