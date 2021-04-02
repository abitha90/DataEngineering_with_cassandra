# DataEngineering_with_cassandra
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. 
The analysis team is particularly interested in understanding what songs users are listening to. 
Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

# Project Steps:
   1. Modelled the data using Apache Cassandra to create tables, insert data and to run queries.
   2. ETL pipeline transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.
   
#Files:
  1. event_data - Data set, directory of csv files partitioned by date
  2. event_datafile_new.csv - File created by ETL pipeline and contains denormalized data set
   
