# Data Modeling with Postgres - Sparkify

## Summary:

A new music streaming startup company named Sparkify is wanting to analyze the data they collect on songs and user activity. Their analytics team wants to understand the songs their users listen to, but they currently don’t have an easy way to query the data. They would like a database created with tables designed to optimize queries for song and user activity analysis.  

This project's goal is to create a Postgres database using the star schema design which is used for query optimization and ETL pipeline to transfer data from the song and user activity logs to data tables. These tables are to be designed to optimize queries on song play analysis which will help the analytics team answer questions about their user's activity.


## Data

There are two data files. The log_data and the song_data files. These files are located in the data folder in the project workspace. Each file is in JSON format and contains metadata about each song and the song's artist. These files are read into panda dataframes.


## Project Workspace Files
  
- **test.ipynb** tests your code by displaying the first few rows of each table to check your database.
- **create_tables.py** this file first drops and then creates the tables. Running this file resets the tables before the ETL scripts run.
- **etl.ipynb** this file reads and processes a single file from song_data and log_data. It then loads the data into the tables. 
- **etl.py** reads and processes files from song_data and log_data and loads the data into the tables. 
- **sql_queries.py** this file contains all the sql queries, It is imported into the create_tables.py, etl.ipynb and etl.py files.
- **README.md** provides information on the project.


## Data Model: Star Schema
![Data Model Star Schema2](https://github.com/mstrish33/DataModeling/assets/139257070/741e53da-f5b2-4dff-918b-f01f9b03f668)

The star schema design is multi-dimensional and optimized for querying data. It has one fact table and multiple dimension tables.
  
- Fact table: songplays
- Dimensions tables: users, time, artist and songs


## Steps for Running Python Script

1. Run the ETL Process file (etl.ipynb).
    - This file will first import the necessary libraries.
    - Run the create_tables.py file in terminal to delete any existing old tables and create new database tables.
    - Connects to the database.
    - It gets and reads the JSON files
    - Inserts a record in each of the tables for testing
    - closes the connection

2. Run the etl.py file in terminal to process and load the data into the tables.
3. To ensure the data loaded correctly, run the test.ipynb file.


