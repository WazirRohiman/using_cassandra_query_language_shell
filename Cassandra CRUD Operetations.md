Prep the environment and connect to command line
```
start_ cassandra

CREATE KEYSPACE training WITH replication = {'class':'SimpleStrategy', 'replication_factor': 3};

use training;

CREATE TABLE movies (movie_id int PRIMARY KEY, movie_name text, year_of_release int);
```

Insert the first row into the table 
```
INSERT into movies(
movie_id, movie_name, year_of_release)
VALUES (1, 'Toy Story', 1995)
```

Verify that the data is saved
```
SELECT * FROM movies;
```

Insert the following rows
```
INSERT into movies(
movie_id, movie_name, year_of_release)
VALUES (2, 'Jumanji', 1995);

INSERT into movies(
movie_id, movie_name, year_of_release)
VALUES (3, 'Heat', 1995);

INSERT into movies(
movie_id, movie_name, year_of_release)
VALUES (4, 'Scream', 1995);

INSERT into movies(
movie_id, movie_name, year_of_release)
VALUES (5, 'Fargo', 1996);
```

Query movie_name with movie_id = 1
```
 SELECT movie_name FROM movies WHERE movie_id-1;
```

The movie_id for Scream is 4. It was released in 1996 and not 1995
Use the command below to modify it
```
UPDATE movies
SET year_of_release = 1994
WHERE movie_id = 4;
```

Delete movie with movie_id = 5
```
DELETE from movies
WHERE movie_id = 5;
```
