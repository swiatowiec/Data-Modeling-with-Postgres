# Summary

Sparkify - a music streaming startup wants to analyze the collected data. The data resides on a directory of JSON logs on user activity so they don't have an easy way to query data. In order to enable Sparkify to create queries and to facilitate data analysis, a Relational Database and ETL papieline ware created. 

## How to run the scripts

To create the database tables and run the ETL pipeline, you must run the following two files in that order:
To create tables:
```bash
python3 create_tables.py
```
To fill tables via ETL:
```bash
python3 etl.py
```
## The project file structure

 - `sql_queries.py` - contains all sql queries, and is imported into the last three files above
 - `create_tables.py` - drops and creates your tables
 - `etl.py` - reads and processes files from song_data and log_data and loads them into your tables
 - `etl.ipynb` - eads and processes a single file from song_data and log_data and loads the data into tables
 - `test.ipynb` - displays the first few rows of each table to let you check your database
 - `README.md` - provides discussion on project
 


> Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.

The purpose of this database is for all users to easily, quickly and intuitively execute queries on sparkify application data resource analysis. This database was created using Spark. The main advantage of Spark is that this framework allows you to analyze and process large data sets, but also allows you to use SQL.


> State and justify your database schema design and ETL pipeline.

The database is organized according to the star schema with different dimension tables linked to a central fact table that shows a transaction important to the company. Use Spark to access each table.

