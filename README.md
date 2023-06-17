# Home_Sales - Big Data


This Challenge uses SparkSQL tool to determine key metrics about home sales data; 
33,288 rows taken from a CSV file. Get the file in this web link:

https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv

As an exercize to manage big data, it will be created a temporary table, partition the data based a date field, and compare the execution time between the options, in order to get the best way to optimize the query execution in this example.

to see the code used in this project.
In the next part, you will see just comparison of the same query with different optimization strategies.

# PART 1

See the execution time of a regular query (with no optimization at all) --> 1.0082 sec

<p align="center"><img src="https://github.com/zuntaalejandra/Home_Sales/blob/main/Images/SQL_No_Cache.png" /></p>


# PART 2

See the execution time of the same query (after upload in cache the table) --> 0.6479 sec

<p align="center"><img src="https://github.com/zuntaalejandra/Home_Sales/blob/main/Images/SQL_In_Cache.png" /></p>


# PART 3

Execute partition of the table based on a "date_built" field 

<p align="center"><img src="https://github.com/zuntaalejandra/Home_Sales/blob/main/Images/Exc_Partition.png" /></p>

See how  it is seen the partitions in Google colab 

<p align="center"><img src="https://github.com/zuntaalejandra/Home_Sales/blob/main/Images/Partitions_created.png" /></p>


# PART 4

See the execution time of the same query (after partition process) --> 0.6687 sec

<p align="center"><img src="https://github.com/zuntaalejandra/Home_Sales/blob/main/Images/SQL_with_Partitions.png" /></p>


# CONCLUSION


To manage big data, is always recomended to use one of the previous  strategies to optimize the response time of queries (also hints in query can be used). 
