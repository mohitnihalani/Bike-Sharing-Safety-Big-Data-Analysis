# How Safe is Bike Sharing: A Big Data Analysis?

## Abstract
With the increasing popularity of the bike sharing programs in NYC, there has been increasing concerns regarding the safety of riders, mainly because the NYC has high traffic and also
it is not mandatory for bike sharing riders to wear helmets. This paper performs the big data analysis on NYC Vision Zero, Citi Bike, and Weather dataset to analyze the pattern between the
accidents and city bikes. We analyzed which areas are more prone to accidents and which are not and what is the probability of the Citi bike riders to meet an accident and is there any correlation
between growth of city bike popularity and increasing bike accidents in NYC. This research can be further used to identify the reasons of high accidents in the given area compared to other and resolve safety issues, by efficient planning of bicycle lanes, regulating traffic or even posting traffic officers in the areas of high bicycle accidents.

## Datasets
1. [Motor Vehicle Crash](https://data.cityofnewyork.us/Public-SafetyNYPD-Motor-Vehicle-Collisions-Crashes/h9gi-nx95)
2. [NYC Weather Data](https://www.ncdc.noaa.gov/)
3. [NYC Citi Bike Data](https://s3.amazonaws.com/tripdata/index.html)

## Code Structure

### 1. /Data Ingest
- /WeatherData-Ingest: It contains the command for ingesting weather datasets into the HDFS. 
- /CitiBike-Ingest: It contains the command for ingesting Citi bike datasets into the HDFS. 
- /Accidents-Ingest: It contains the command for ingesting accidents datasets into the HDFS.

### 2. /Profiling Code
- /WeatherProfiling: It contains the map reduce for profiling weather data.
- /CitiBikeProfiling: It contains the map reduce for profiling Citi bike data.
- /AccidentsProfiling: It contains the map reduce for profiling accidents data.

### 3. ETL
It  contains the Map Reduce code for preprocessing the datasets. The following methods are done in preprocessing.
- /WeatherETL: It contains the map reduce for cleaning weather data.
- /CitiBikeETL: It contains the map reduce for cleaning Citi bike data.
- /AccidentsETL: It contains the map reduce for cleaning accidents data.
- /lat-long : It contains local python code for extracting zip codes using latitude and longitude for accidents and Citi bike dataset.
    - /citibike/extractzipcode.py -> extracting zip code of Citi Bike 
	- /accidents/read.py --> ConvertingLatLong for accidents data.

### 4 Code Iterations: 
- This directory consists of java files that didn't make it to the final code.

### 5 Source Code for the analytics 
- this directory contains the hive queries which were used for the analytics.

### 6. Outputs 
- It  contains the screenshots of the analytics

## Team Members:

1. Mohit Nihalani
2. Hardik Bharath Rokad
3. Rohit Saraf