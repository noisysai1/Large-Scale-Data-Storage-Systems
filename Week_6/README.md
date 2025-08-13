Week 6 – AWS RDS, S3 Data Integration and SQL Analytics

Sai Kumar Murarishetti

🗃️ Objective

In Week 6, the focus was on end-to-end cloud-based data processing using AWS services like S3 and RDS, paired with Linux command-line data cleaning and SQL analytics.
The dataset used was a large airline CSV file from September 2012 with nearly 490,199 rows.

✅ Task Breakdown
📥 1. Data Preprocessing in Linux

File Used: Sai-sep2012.csv

Cleaned the dataset before uploading to the cloud:

Removed the header using the sed command:

sed -i '1d' Sai-sep2012.csv


Verified line counts before and after using:

wc -l Sai-sep2012.csv

Confirmed that the first line (headers) was removed.

☁️ 2. Uploading to AWS S3

Uploaded the cleaned CSV file (Sai-sep2012.csv) to an Amazon S3 bucket.

This allowed for scalable storage and easy integration with AWS RDS.

The upload was successful and verified through the AWS Console.

🛢️ 3. AWS RDS Instance Setup

Created a MySQL-compatible RDS instance.

Connected to the RDS instance using a MySQL client.

Created a database and table schema matching the structure of the CSV file.

Loaded the S3 data into the RDS table using:

LOAD DATA FROM S3 ...

🧮 4. SQL-Based Data Analysis

Ran multiple SQL queries to analyze the airline dataset:

Query	Description	Result
4a	Total number of flights	490,199
4b	Total flights operated by United Airlines (Carrier code 19977)	42,806
4c	Number of cancelled United Airlines flights	257
4d	Total United Airlines flights from Chicago O'Hare to Los Angeles	312
4e	Number of delayed flights from O'Hare to Los Angeles for United Airlines	72
4f	Total cancellations by American Airlines and United Airlines combined	1,304
4g	Total delayed United Airlines flights across all origins and destinations	9,324
🧾 5. Final Stats Summary

Name: Sai Kumar Murarishetti

Month of Data: September 2012

File Records: 490,199

Header Removed: ✅ (Confirmed with wc -l)

Uploaded to S3: ✅

Loaded to RDS: ✅

Queried Successfully: ✅

🧹 6. Resource Cleanup

To prevent unnecessary charges:

Stopped and deleted the RDS instance after query execution.

Deleted the S3 bucket and uploaded data after verification.

📌 Key Learnings

✨ Data Cleaning in Linux:
Learned to use sed, wc, and head for efficient CSV manipulation.
✨ AWS S3 Integration:
Uploaded data to Amazon S3 and used it as a source for RDS import.
✨ RDS Setup and Querying:
Created MySQL-compatible RDS, built schema, and queried millions of rows using SQL.
✨ Query Optimization:
Used carrier codes, origin/destination filters, and conditional queries to extract targeted insights.
✨ Cloud Resource Management:
Practiced stopping/deleting AWS resources post-usage to optimize cost.

📁 Folder Structure
Week-6/
├── data/
│   └── Sai-sep2012.csv
├── cleaned/
│   └── Sai-sep2012_cleaned.csv
├── preprocessing/
│   └── sed_wc_commands.txt
├── sql/
│   └── airline_queries.sql
├── screenshots/
│   ├── sed_wc_verification.png
│   ├── s3_upload.png
│   ├── rds_query_results.png
│   ├── instance_stopped.png
│   └── bucket_deleted.png
└── README.md


