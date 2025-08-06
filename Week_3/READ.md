📅 Week 3 - Cloud Cost Estimation, Service Models, and Productivity Tools
Student: Sai Kumar Murarishetti

🔹 Project 1: AWS EC2 Server Cost Estimations
I used the AWS Pricing Calculator to estimate costs for different server setups:

Linux Server: 9 servers, each with 40 GB EBS.
Red Hat Server: 8 servers, each with 40 GB EBS.
Alternative Red Hat Server: 7 servers, each with 40 GB EBS.
Windows Server: 6 servers, each with 40 GB EBS.

Key Takeaways:
Reserved Instances:

3-year reserved plans cost less than 1-year plans.
Offer discounts compared to on-demand pricing.
Guarantee server availability even during high demand.

Regional Pricing:

Costs vary by location. Example:
Red Hat → $46.87 (Oregon) vs $47.87 (Ireland).
Windows → $3.80 (Oregon) vs $4.31 (Ireland).

OS Cost Difference: Windows EC2 servers are more expensive than Red Hat.

Payment Options:

Partial Upfront: Pay part now, lower monthly fees.
Full Upfront: Pay all at once; biggest overall savings.
Spot Instances:
Very cheap, but not reliable for critical 24/7 apps since AWS can terminate them anytime.

🔹 Project 2: Cloud Service Model Selection

For a small startup using Java and Python, I chose Platform as a Service (PaaS).
IaaS (Infrastructure as a Service): Provides servers and networking but requires heavy management.
PaaS (Platform as a Service): Best option. It provides development frameworks, runtime, and scaling so developers focus on coding.
SaaS (Software as a Service): Ready-made software; less flexible for startups needing custom apps.

Platform Comparisons:
AWS Elastic Beanstalk:
Supports Java & Python.
Handles load balancing, scaling and app monitoring automatically.
Integrates easily with other AWS services.

Google App Engine:
Serverless PaaS.
Automatically scales apps with demand.
Offers real-time collaboration features.

Heroku:
Easy app deployment and management.
Supports multiple languages.
Provides Heroku Postgres database.
Great for startups due to simplicity and quick setup.

🔹 Project 3: Productivity Tools Comparison
I compared Microsoft Office, LibreOffice, and Google Docs/Sheets.
Microsoft Office: Paid, professional with yearly plans.

LibreOffice:
Free, open-source.
Works offline.
Compatible with Microsoft Office formats.

Google Docs/Sheets:
Cloud-based, free.
Supports real-time collaboration.
Accessible on any device with internet.

Conclusion:
LibreOffice is best if you want offline use at no cost.
Google Docs/Sheets is better for teams needing online collaboration.

📌 Key Learnings from Week 3
Learned to use the AWS Pricing Calculator for server cost estimation.
Understood cost-saving strategies like Reserved Instances and trade-offs of Spot Instances.
Chose the best cloud service model (PaaS) for a startup needing Java/Python support.
Gained insights into collaboration tools, weighing LibreOffice (offline) vs Google Docs/Sheets (online).

📂 Recommended GitHub Folder Structure

Week-3/
├── AWS_Cost_Estimations.txt
├── Cloud_Service_Model_Analysis.txt
├── Productivity_Tools_Comparison.txt
├── Screenshots/
├── README.md
