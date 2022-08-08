# ETL Pipeline for Sparkify using Postgres

This project is to build ETL pipeline for Sparkify:music streaming app. This builds Star schema using Fact and Dimension tables in Postgres and inserts data into new tables. Project aims to analyse what songs users are listening to on Sparkify app.


## Explanation of file structure

```
|____data # Dataset
| |____log_data
| |____song_data
|
|____notebook # notebook for developing and testing ETL
| |____etl.ipynb # developing ETL builder
| |____test.ipynb # testing ETL builder
|
|____src # source code
| |____etl.py # ETL builder
| |____sql_queries.py # SQL query statements 
| |____create_tables.py # database/table creation script
```

## How to run python scripts

Ensure you've python installed 

To create database and tables run
```python create_tables.py```

To run ETL pipeline
```python etl.py```



## Star Schema
```
songplays - Fact Table
	- songplay_id 	PRIMARY KEY
	- start_time 
	- user_id
	- level
	- song_id 
	- artist_id
	- session_id
	- location
	- user_agent
```

```
users - Dimension Table
	- user_id 	PRIMARY KEY
	- first_name
	- last_name
	- gender
	- level

songs - Dimension Table
	- song_id 	PRIMARY KEY
	- title
	- artist_id
	- year
	- duration

artists - Dimension Table
	- artist_id 	PRIMARY KEY
	- name
	- location
	- latitude
	- longitude

time - Dimension Table
	- start_time 	PRIMARY KEY
	- hour
	- day
	- week
	- month
	- year
	- weekday
```
