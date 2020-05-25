## Project-3-Data-Warehouse

Udacity Data Engineer     
Here's a [guide](https://www.markdownguide.org/basic-syntax/) on Markdown Syntax.

### Introduction

A music streaming startup, Sparkify, has grown their user base and song database and want to move their processes and data onto the cloud. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

### Project Description
In this project, we built an ETL pipeline that extracts their data from S3, stages them in Redshift, and transforms data into a set of dimensional tables for their analytics team to continue finding insights in what songs their users are listening to. 

### Database schema design and ETL pipeline
We implemented the Star Schema for this project, with one fact table (songplays) and four dimension tables (users, songs, artists, and time).

### Files
In addition to the data files, the project workspace includes six files:

* 1. create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
* 2. etl.py loads data from staging tables to analytics tables on Redshift
* 3. dwh.cfg contains the login information to Amazon.

### Data
You'll be working with two datasets that reside in S3. Here are the S3 links for each:

* Song data: s3://udacity-dend/song_data  
* Log data: s3://udacity-dend/log_data  

Log data json path: s3://udacity-dend/log_json_path.json


### Song Dataset
The first dataset is a subset of real data from the [Million Song Dataset](http://millionsongdataset.com/). Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID.  

And below is an example of what a single song file, TRAABJL12903CDCF1A.json, looks like.

    {"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}

### Log Dataset
The second dataset consists of log files in JSON format generated by this [event simulator](https://github.com/Interana/eventsim) based on the songs in the dataset above. These simulate activity logs from a music streaming app based on specified configurations.




