📅 Week 7 – Data Format Conversion using AWS Glue

 Sai Kumar Murarishetti


Objective

This week's task focused on data format conversion using AWS Glue. The assignment involved uploading large CSV files, preprocessing them, and converting them into more efficient data storage formats like ORC and Parquet using different compression algorithms (Snappy and Gzip). The goal was to analyze and compare file sizes post-conversion to understand their storage impact in cloud environments.

✅ Task Breakdown
📁 Step 1: File Preparation

Files used:

September2012.csv
October2012.csv
November2012.csv

Actions Performed:

Transferred all files to an EC2 instance.

Unzipped the files.

Used the head command to inspect file content.

Removed headers from the 2nd and 3rd files using:

sed -i '1d' October2012.csv
sed -i '1d' November2012.csv


Combined the files using:

cat September2012.csv October2012.csv November2012.csv > combined.csv


Verified total line count using:
wc -l combined.csv


✅ Line Count: 1,493,460

☁️ Step 2: Upload to AWS and Table Creation

Uploaded the combined CSV (combined.csv) to an S3 bucket.

Used AWS Glue to:
Create a crawler to catalog the dataset.

Create a Glue job to convert CSV to:
ORC
Parquet with Snappy
Parquet with Gzip


🔁 Step 3: Data Format Conversion
Format	Compression	File Size
CSV (original)	—	57.3 MB
ORC	Snappy	1.4 MB
Parquet	Snappy	1.7 MB
Parquet	Gzip	1.2 MB

🟢 Result: The ORC and Parquet formats significantly reduced file sizes — up to 97.9% smaller than the original CSV.

🧠 Observations & Learnings

Storage Efficiency:
Compression via ORC and Parquet greatly optimizes storage without data loss.

Cost Savings:
Smaller files = lower storage and transfer costs in cloud platforms.

Format Suitability:
ORC is ideal for analytics with Hive.
Parquet is widely used with AWS Athena, Spark, and more.

Tool Used:
✅ AWS Glue (Option #1) — fully managed ETL service.

📦 Metadata Summary
Field	Value
Student Name	Sai Kumar Murarishetti
Student ID	30079224
Month & Year of Files	Sept 2012, Oct 2012, Nov 2012
Total Combined Lines	1,493,460
Original CSV File Size	57.3 MB
Parquet (Snappy) File Size	1.7 MB
ORC File Size	1.4 MB
Parquet (Gzip) File Size	1.2 MB
AWS Tool Used	AWS Glue

🧹 Final Cleanup

✅ Deleted temporary tables and databases created in AWS Glue and the Data Catalog to avoid unnecessary billing.


📁 Folder Structure
Week-7/
├── raw_data/
│   ├── September2012.csv
│   ├── October2012.csv
│   └── November2012.csv
├── combined/
│   └── combined.csv
├── cleaned/
│   └── combined_no_header.csv
├── scripts/
│   └── remove_headers.sh
├── aws_glue_jobs/
│   ├── glue_job_parquet_snappy.py
│   ├── glue_job_parquet_gzip.py
│   └── glue_job_orc.py
├── screenshots/
│   ├── upload_to_s3.png
│   ├── glue_conversion_results.png
│   └── storage_comparison.png
└── README.md
