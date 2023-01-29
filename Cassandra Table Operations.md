After connecting to Cassandra server and creating a keyspace called training with replication class Simple Strategy and factor 1, creates a table named movies, in the training keyspace.

The movies table has three columns:
```
    ‘movie_id’ is an integer and is the primary key.
    ‘movie_name’ is a text column.
    ‘year_of_release’ is an integer.
```

Use ```describe tables;``` to see the tables in the keyspace

Use ```describe movies;``` to see the 'movies' tables in the keyspace

Use teh command below to modify it by adding a column named ‘genre’ which is of type ‘text
```
ALTER TABLE movies
ADD genre text;
```

So example commandss
```
CREATE TABLE movies( movie_id int PRIMARY KEY, movie_name text, year_of_release int);
```

```
ALTER TABLE movies ADD genre text;
```


