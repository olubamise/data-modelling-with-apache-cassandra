# Document Process

**Version: 1.0.
Approved By: Joseph Aiyeoribe.
Date: July 3, 2021.**<br>

#### Project description
This project involves creating Apache Cassandra No SQL database tables designed to optimize queries on song played analysis. It involves data modelling with Apache Cassandra and scripting ETL pipelines that analyses and transfer data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables. These data are filtered and stored on the Appache Cassandra No SQL database tables.

The project was designed using Appache Cassandra, Jupyter Notebook and Python programming language.

#### Database Template
1. processed the event_datafile_new.csv dataset to create a denormalized dataset
2. modelled the data tables keeping in mind the queries you need to run
3. create queries that is needed to model the data tables
4. loaded the data into tables that were created in Apache Cassandra and run the queries

#### Table Description
# Table 1
artist_song_length_session_table - records users song information. 

*sessionid INT*<br>
*iteminsession SMALLINT*<br>
*song TEXT*<br>
*artist TEXT*<br> 
*length FLOAT*<br>
PRIMARY KEY (sessionid, iteminsession)*<br>

# Tables 2
artist_song_user_session_table - records artists information. 

*userid SMALLINT*<br> 
*sessionid INT*<br>
*iteminsession SMALLINT*<br> 
*firstname TEXT*<br> 
*lastname TEXT*<br>
*artist TEXT*<br>
*song TEXT*<br>
*PRIMARY KEY ((userid, sessionid), iteminsession)*<br>

# Tables 3
user_song_table - records users songs information.
 
*song TEXT*<br>
*userid INT*<br>
*firstname TEXT*<br>
*lastname TEXT*<br>
*PRIMARY KEY (song, userid)*<br>

### ETL Process
All the extraction, transformation and loading of data is done by the ETL script of the project. Data is read and processed from set of CSV files within a directory. It is then loaded into the Apache cassandra database tables. The ETL step by step activities includes:<br>

1. processed the event_datafile_new.csv dataset to create a denormalized dataset
2. modelled the data tables keeping in mind the queries you need to run
3. create queries that is needed to model the data tables
4. loaded the data into tables that were created in Apache Cassandra and run the queries

The Anaytics team is mostly interested in the clean data that is ingested into the data table and that is where the optimize queries on song played will be analysed.<br>
    
#### Project Files Repository
Below are the important project files and information about what they are used for:

1. Project_1B_ Project_Template1.ipynb - is the jupyter notebook file that contains the project. no SQL and ETL are all included on the file.
2. event_datafile_new.csv - is the streamlined csv file that is created to extract data from a set of CSV files within a directory (primary data sources) 
3. README.md - is a plain text file that provides information abouot the project and how it runs.<br>

#### Steps to Run The Project
1. Click on Run menu on Jupyter Notebook. 
2. From the Run menu drop down, click on Selected Cell to run individual cells.
