# Managing Big Data

## For this assignment, you will create a table with data describing an underground tunneling project.

1. If you took the second course in this specialization (Analyzing Big Data with SQL), recall that the assignment asked you to analyze flights data to select a profitable route for an underground high-speed rail tunnel. 
2. Based on your analysis and on other factors, construction has begun on a tunnel connecting San Francisco and Los Angeles. 
3. The tunnel will be dug over a period of ten years. 
4. It will be dug in three different sections by three tunnel boring machines (TBMs) named 
    - Bertha II 
    - Shai-Hulud, and 
    - Diggy McDigface.

Each of these TBMs will generate a large volume of data as it operates. 
Each TBM will generate the data slightly differently. 
Simulated versions of the three TBM-generated datasets are provided. 
You must create a table on the VM and load these datasets into it. 
Then you must create and upload a document describing the steps you performed to complete this task.

### Examine the Data

- Use the commands you learned about in this course to list and examine the three files containing the tunnel boring machine data. 
- They are delimited text files, each containing tens of thousands of lines. 
- They are stored in `Amazon S3` in subdirectories under a directory named tbm_sf_la in the `S3 bucket named training-coursera2`. You have read access to this bucket.

Hint: List these files and view their contents by running commands in the terminal. Use chaining to apply the head command to display only the first few rows of each file.

- Notice what these three files have in common:
    - Each file contains eight columns representing the same eight fields
    - The data types of the eight columns are the same in all three files
    - The rows of the table represent hourly time intervals
    - Notice the differences between these three files:

1. They use different delimiters
2. One of the files uses the string `999999` to represent missing values
3. One of the files has a header line

### Create the Table

Create a table named **tbm_sf_la** in the database named **dig** to store the data from all three of the TBMs. Use what you learned by examining the data to decide how best to do this.

W​hen creating this table, you must:
1. Use the exact column names shown in the header line in one of the files
2. Specify appropriate data types for the columns, based on what you observed when examining the data and based on what you have learned about data types in this course
3. Ensure that the table can be queried by both Hive and Impala