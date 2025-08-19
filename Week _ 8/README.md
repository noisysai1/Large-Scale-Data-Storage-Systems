Week 8 – Securing AWS Resources Using IAM, S3 Policies and Security Groups

Sai Kumar Murarishetti

🧾 Objective

This week’s task focused on AWS resource security. 
The goal was to create IAM users with restricted and specific access permissions, apply S3 bucket policies and configure EC2 security groups to control inbound/outbound network access.
The activity also included hands-on testing of permissions and simulating access control across different user roles.

✅ Part 1: IAM User and Role-Based Access Configuration

👥 IAM Users Created:

FinUser
ITUser
AirlineUser

🔒 Access Testing Results:
Action	FinUser	ITUser	AirlineUser
View EC2 Instances	❌	✅	❌
View Billing Information	✅	❌	❌
Access S3 Bucket	✅	✅	❌ (initially)

FinUser: Granted access to billing only. Cannot see EC2 instances.
ITUser: Can access EC2 instances and S3, but not billing.
AirlineUser: Initial configuration denied access to both EC2 and S3. Later modified.

✅ Part 2: S3 Bucket Policy and Permissions Testing

🔐 Steps Performed:

Created an S3 bucket.
Uploaded sample files into the bucket.
Used the AWS Policy Generator to define custom S3 access permissions.
Applied the bucket policy via the AWS Management Console.

🔍 Result of Access Tests:

IAM User	Access to S3 Bucket
AirlineUser	✅ (after policy update)
ITUser	❌
FinUser	❌

Only AirlineUser was granted bucket access via policy.

Verified that other users were blocked, confirming the effectiveness of the bucket policy.

✅ Part 3: EC2 Instance & Security Group Management

🖥️ Actions Taken:

Launched EC2 instance.
Noted the public and private IP addresses.
Logged out of connected terminal to simulate remote access.
Modified inbound security rules of the EC2 instance’s security group.

🔐 ICMP (Ping) Testing:
Scenario	Result
Ping without ICMP rule	❌ Timeout
Ping after adding ICMP (All traffic allowed)	✅ Success
Ping after removing ICMP again	❌ Timeout
🧹 Final Actions:

Stopped EC2 instance.

Deleted S3 bucket and terminated all created resources to avoid unnecessary billing.

🧠 Key Learnings

Understood IAM best practices for least privilege access.
Practiced S3 bucket policy creation and tested real-world access scenarios.
Gained experience with network control using EC2 security groups, especially with ICMP testing.
Reinforced AWS cost-management discipline by cleaning up resources after testing.

📁  GitHub Folder Structure
Week-8/
├── iam_users_config.txt
├── s3_bucket_policy.json
├── ec2_security_group_changes.txt
├── screenshots/
│   ├── user_access_tests.png
│   ├── billing_visibility_finuser.png
│   ├── s3_policy_generator.png
│   ├── icmp_ping_success.png
│   └── final_cleanup.png
└── README.md
