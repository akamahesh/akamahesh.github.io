---
layout: post
title: The Sequel to SQL Part-2
date: 2017-12-15 00:00:00 +0300
description: Advance SQL # Add post description (optional)
img: sql-sequel.png # Add image post (optional)
tags: [SQL, database] # add tag
---

# The Sequel to SQL:
Level 3- section 1
### Nomalization
- Normalization is the process of reducing duplication in database tables.   
- First Normal Form Rule : Tables must not contain repeating groups of data in 1 column.  
- Second Normal Form Rule : Tables must not contain redundancy.  
- Join Table :  Creating a Join Table Movies_Genres for mapping  

- Updating Movie Information Is Easier like To update a movie duration  
```SQL
UPDATE Movies
SET duration = 134
WHERE id = 2;
```

- To add a genre to a movie:

```SQL
INSERT INTO Movies_Genres (movies_id,genre_id)
VALUES (4,3);
```

**Q How do we find the genres of Peter Pan?**
Feteches the id  
```SQL
SELECT id
FROM Movies  
WHERE title = "Peter Pan";
```

Feteches the genres_id for our Movies_Genres table  
```SQL
SELECT genre_id
FROM Movies_Genres  
WHERE movie_id = 2;
```

Feteches the genre names for own movie  
```SQL
SELECT name
FROM genres
WHERE id = 2 or id =3;
WHERE id IN (2,3);
```

## Level3 - Section2  Relationships  

- 3 Different Types of Table Relationships  
> one to one
> one to many
> many to many

-
