Week 4 – AWS Cloud Storage Cost Estimation & S3 Operations
Sai Kumar Murarishetti


✅ Part 1: AWS Cloud Storage Cost Estimations (via AWS Calculator)
Used the AWS Pricing Calculator to estimate and compare costs for storing large datasets (420 TB and 4.2 PB) across different AWS storage services.

💾 Storage Cost Comparisons:
Storage Type	Volume	Estimated Cost
S3 Standard	420 TB	View Estimate
S3 Standard	4.2 PB	[View Estimate]
EBS	420 GB	Calculated separately
EBS	4.2 PB	$430,080.00 without snapshots
S3 Glacier	420 TB	[View Estimate]
S3 Glacier	4.2 PB	[View Estimate]

🔍 Additional Insights:
Cheapest Option: S3 Standard

Most Expensive : EBS (Elastic Block Store)

✅ Part 2: Impact of Snapshots on EBS Pricing
Added 2x Daily Snapshot Frequency for EBS (4.2 PB):

Original EBS cost: $430,080.00

After Snapshots: Increased by $216,217.90

✅ Conclusion: Snapshot frequency significantly increases EBS storage cost

✅ Part 3: Data Transfer Calculations

⏱️ Uploading 420 TB @ 55 Mbps
Used Tool: Omni Data Transfer Calculator

Upload Time:
Approx 88 days to upload 420 TB at 55 Mbps

📤 Download Cost from AWS S3
Calculated the cost of downloading 420 TB from S3 to home/office via internet

✅ Used AWS Calculator to simulate and record download cost

(Screenshots included in assignment PDF)

🌍 Inter-Region Transfer Cost
Calculated 420 TB transfer from Frankfurt ➝ Oregon

Used AWS Calculator to determine inter-region transfer fees

(Estimate shown in screenshots)

✅ Part 4: AWS S3 Hands-on Tasks (from Assignment2 - Cloud Storage)
Performed file and folder operations using S3 tools/CLI:

📁 S3 File System Commands:

Created folders and subfolders using mkdir
Created both .txt and binary files
Uploaded files to AWS S3
Created a .txt file in Folder 2
Shared the .txt file (not the binary file)
Deleted files/folders recursively
Synced folders using sync
Checked object sizes
Verified that S3 bucket list was empty initially

📌 Summary of Learnings
Learned to calculate and compare AWS storage costs for various services (S3, EBS, Glacier).
Understood the cost impact of snapshots and data transfers.\
Practiced hands-on S3 operations like uploading, syncing, sharing and deleting files.
Developed awareness of region-based pricing differences and download vs inter-region costs.

📁GitHub Folder Structure:

Week-4/
├── Storage_Cost_Estimations.txt
├── Data_Transfer_Calculations.txt
├── AWS_S3_HandsOn_Commands.txt
├── Screenshots/
│   ├── AWS_Calculator_EBS.png
│   ├── S3_Download_Cost.png
│   └── Transfer_Time_Estimate.png
└── README.md
