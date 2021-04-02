# DataEngineering_with_cassandra
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. 
The analysis team is particularly interested in understanding what songs users are listening to. 
Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

#PROJECT APPROACH:
    1.Modelled the data using Apache Cassandra to create tables, insert data and to run queries.
    2.ETL pipeline transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.
    
#Files:
    1. event_data - Data set, directory of csv files partitioned by date
    2. event_datafile_new.csv - File created by ETL pipeline and contains denormalized data set
    
    
#TABLES AND QUERIES USED TO MODEL DATA:
    1. music_history_q1
        Partitioning column: sessionId, 
        Clustering column: itemInSession
        Query: SELECT * FROM music_history_q1 WHERE sessionId = 338 AND itemInSession = 4

        
    2. music_history_q2
        Partitioning column: userId, 
        Clustering column: sessionId
        Query: SELECT * FROM music_history_q2 WHERE userId=10 AND sessionId = 182
         
    3. music_history_q3
        Partitioning column: song
        Query: SELECT * FROM music_history_q3 WHERE song ='All Hands Against His Own'
   
