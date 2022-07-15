# Streaming Data Logs ETL Pipeline to PostGres using Python

## Asignment 1: Udacity Data Enginnering
***
Using the psycopg2 and pandas libraries, json logs for user events and song data
are processed and loaded into a PostGres WareHouse to easy analytics and data
management.
***
Contents: 
1. Data Folder: the data is in the data folder in the folder root with two folders
    1. log_data: JSON Log files with user, artist, song and timestamp data
    2. song_data: JSON song data

2. Python Scripts in Folder root
    1. sql_queries.py - PostGres Queries to Create/Delete Database tables, insert data and query for a specific song
    2. create_tables.py - imports queries, re-creates/creates database, and all tables
    3. etl.py - imports queries, processes JSON files and loads into Database

3. Ipython Notebooks in Folder root
    1. etl.ipynb - test run of ETL on one file
    2. test.ipynb - tests database schema, constraints and loaded data

### To run first create tables, then run ETL, to re-run ETL re-create the tables/database

## ***Changelog since review (Very good feedback from Reviewer)***
1. Updated README
2. Added Doc Strings to ETL
3. Updated User table insert to update level on conflict from DO NOTHING
4. Updated primary key of songplay to BIGSERIAL
5. Changed Variables from python syntax to PostGRES Syntax e.g int to INT, text to VARCHAR
6. Added NOT constraints to several foreign keys
7. Added a primary key for the time dimension table
8. Updated song select querry to use difference in time of less than 0.01 seconds, the equality operator was not working.


### ***Obira Daniel, July 2022***