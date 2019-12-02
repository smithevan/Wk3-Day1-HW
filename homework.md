# SQL Homework

The Springfield Cinema is having a Marvel Movie Marathon! They have asked you to help maintain their database of movies with times and attendees.

## To access the database:

First, create a database called 'marvel'

```
# terminal
createdb marvel
```

Next, run the provided SQL script to populate your database:

```
# terminal
psql -d marvel -f marvel.sql
```

Use the supplied data as the source of data to answer the questions. Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.

## Questions

1.  Return ALL the data in the 'movies' table.

SELECT * FROM movies;
id |                title                | year | show_time
----+-------------------------------------+------+-----------
 1 | Iron Man                            | 2008 | 18:10
 2 | The Incredible Hulk                 | 2008 | 16:45
 3 | Iron Man 2                          | 2010 | 19:25
 4 | Thor                                | 2011 | 14:55
 5 | Captain America: The First Avenger  | 2011 | 13:40
 6 | Avengers Assemble                   | 2012 | 18:10
 7 | Iron Man 3                          | 2013 | 18:30
 8 | Thor: The Dark World                | 2013 | 16:50
 9 | Batman Begins                       | 2005 | 21:25
10 | Captain America: The Winter Soldier | 2014 | 12:05
11 | Guardians of the Galaxy             | 2014 | 14:00
12 | Avengers: Age of Ultron             | 2015 | 16:30
13 | Ant-Man                             | 2015 | 12:35
14 | Captain America: Civil War          | 2016 | 20:40
15 | Doctor Strange                      | 2016 | 21:50
16 | Guardians of the Galaxy 2           | 2017 | 19:20
17 | Spider-Man: Homecoming              | 2017 | 13:50
18 | Thor: Ragnarok                      | 2017 | 21:50
19 | Black Panther                       | 2018 | 19:30
(19 rows)

2.  Return ONLY the name column from the 'people' table

SELECT name FROM people;

name        
--------------------
Andrew Gray
Andrew Kirkwood
Andrew Wyper
Catherine Hall
Cosy Abott
Evan Smith
Gary Clark
James Fraser
James Smith
Jamie Ryan
Jen Merritt
Lauren Brett
Luca Sanz Charreun
Matteo Fusillo
Olivia Wright
Patrick ONeill
Ross Cumming
Sigurd Watt
Silvia Simonassi
Stephen Ramsay
Steve Vance
(21 rows)

3.  Oops! Someone spelled Cody Abbott's name wrong! Change it to reflect the proper spelling.

UPDATE people SET name = 'Cody Abbott' WHERE name = 'Cosy Abott';

name        
--------------------
Andrew Gray
Andrew Kirkwood
Andrew Wyper
Catherine Hall
Evan Smith
Gary Clark
James Fraser
James Smith
Jamie Ryan
Jen Merritt
Lauren Brett
Luca Sanz Charreun
Matteo Fusillo
Olivia Wright
Patrick ONeill
Ross Cumming
Sigurd Watt
Silvia Simonassi
Stephen Ramsay
Steve Vance
Cody Abott
(21 rows)

4.  Return ONLY Olivia Wright's name from the 'people' table.

SELECT * FROM people WHERE name = 'Olivia Wright';

id |     name      
----+---------------
15 | Olivia Wright

5.  The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.


6.  We forgot one of the main characters! Add Chris Fraser to the 'people' table
7.  John Smith has decided to hijack our movie evening, Remove him from the table of people.
8.  The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.
9.  The cinema would like to make the Iron Man movies a triple billing. Find out the show time of "Iron Man 2" and set the show time of "Iron Man 3" to start two hours later.

## Extension

1.  Research how to delete multiple entries from your table in a single command.
