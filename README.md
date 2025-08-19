# Large-Scale-Data-Storage-Systems
DATA-54000__Large Scale Data Storage Systems


📘 Weekly Overview Report (All Week 1 – Week 8)

Student Name: Sai Kumar Murarishetti


✅ Week 1 – VirtualBox & CentOS VM Setup

What I Did

Installed CentOS 7 on VirtualBox.
Created full and linked clones of VMs with different configurations.
Ran basic Linux commands: curl, ping, free -h, echo.
Transferred files between VMs using scp.

What I Learned

VirtualBox VM modes: Normal, Headless, Detachable.
Full vs Linked Cloning.
Snapshot benefits and limitations.
Localhost IP usage (127.0.0.1).
Basics of Linux networking and file management.

✅ Week 2 – Bitnami VM and Hadoop Operations

What I Did

Deployed Bitnami VM and configured memory, CPU, and network adapters.
Verified Hadoop services and tested SSH access via MobaXterm.
Created HDFS folders, uploaded and removed files, used cat, ls, rm, etc.
Uploaded and processed airline data file (Sept 2012) in HDFS.
Modified replication factor and used fsck for file health check.

What I Learned

Using Hadoop Distributed File System (HDFS).
Role of block size and replication in storage.
Hands-on with SSH configuration and firewall rules.
File lifecycle operations in Hadoop.

✅ Week 3 – AWS Pricing and Cloud Service Models

What I Did

Used AWS Pricing Calculator for cost estimation of EC2 servers (Linux, RedHat, Windows).
Compared regional pricing (Oregon vs. Ireland).
Reviewed payment plans: on-demand, reserved (1 yr vs 3 yr), spot instances.
Compared cloud service models: IaaS, PaaS, SaaS.
Studied Elastic Beanstalk, Google App Engine, Heroku.

What I Learned

Cost structures in AWS for compute instances.
Region-based pricing impact.
Pros and cons of cloud service models.
Platform selection for startups using Java/Python.
Spot instances and their risks for 24x7 apps.

✅ Week 4 – AWS Storage (S3, EBS, Glacier)

What I Did

Estimated storage costs for S3, Glacier, and EBS at multiple scales (420 TB, 4.2 PB).
Added EBS snapshot frequency and evaluated cost impact.
Calculated upload/download times and costs using Omni Calculator and AWS Pricing tool.
Tested inter-region data transfer cost (Frankfurt to Oregon).

What I Learned

Trade-offs between S3, EBS, Glacier in terms of cost and performance.
Snapshot frequency affects EBS costs significantly.
Compression and transfer speed affect total time and pricing.
Cloud storage optimization is crucial for large datasets.

✅ Week 5 – AWS EC2 File Transfers, Volumes & CloudFormation

What I Did

Connected to EC2 using MobaXterm.
Transferred files between local machine ↔ VM1 ↔ VM2 ↔ EC2.
Modified EC2 instance type (t3.2xlarge).
Attached/detached/deleted EBS volumes using lsblk.
Deployed new EC2 instances using CloudFormation and deleted them afterward.

What I Learned

Secure file transfer (scp) between instances.
Instance type scaling for performance tuning.
Volume management in EC2.
Automated infrastructure provisioning with AWS CloudFormation.

✅ Week 6 – AWS RDS + S3 + SQL Queries

What I Did

Cleaned airline CSV data (Sep 2012) using sed, head, wc.
Uploaded data to S3, then loaded into RDS (Aurora/MySQL).
Created table schema and ran SQL queries.
Queried flight stats: delays, cancellations, routes, etc.
Stopped and deleted resources to avoid billing.

What I Learned

Full data pipeline: CSV → S3 → RDS → SQL Analysis.
Importance of preprocessing large files.
Efficient SQL querying on cloud databases.
Cloud cost management through cleanup.

✅ Week 7 – CSV to ORC & Parquet Conversion using AWS Glue

What I Did

Removed headers and merged 3 CSVs (Sep, Oct, Nov 2012) → Combined CSV (~1.49M rows).
Uploaded merged file to S3.
Used AWS Glue to convert CSV into:
Parquet (Snappy & Gzip)
ORC (Snappy)
Compared file sizes post-compression.
Deleted Glue tables and S3 resources.

What I Learned

ORC and Parquet provide 90–98% storage savings over raw CSV.
Compression methods (Snappy, Gzip) influence performance and size.
Glue simplifies large-scale ETL workflows without managing infrastructure.
Optimized formats are critical for efficient analytics on big data.

✅ Week 8 – IAM Access Control, S3 Bucket Policies, Security Groups

What I Did

Created IAM users: FinUser, ITUser, AirlineUser.
Configured user-specific access to EC2, billing, and S3.
Created bucket policies using AWS Policy Generator.
Tested user access across S3 and EC2.
Modified EC2 security group inbound rules for ICMP.
Validated ping requests before and after ICMP rules.
Stopped and deleted all instances, buckets, and policies.

What I Learned

Hands-on with IAM and least privilege principle.
Practical application of S3 bucket policies and user testing.
Security group management to allow/deny access based on protocol.
Real-world application of AWS resource security and cleanup discipline.

📌 Final Reflection – Overall Learning Outcomes

🛠️ Technical Skills Gained:

Cloud architecture: S3, EC2, RDS, IAM, EBS, Glue, CloudFormation.
Linux command-line file operations and data prep.
Hadoop and HDFS data processing.
Data format transformation (CSV → ORC/Parquet).
SQL querying at scale on RDS.
Security best practices (IAM, S3 policies, security groups).

💡 Conceptual Understanding:

Cost management in AWS and efficient cloud storage design.
Infrastructure automation and elasticity in the cloud.

Importance of secure access control and minimizing attack surface.

Impact of data format and compression on performance and billing.
