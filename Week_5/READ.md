📅 Week 5 – AWS EC2 Operations, File Transfers & Automation
Sai Kumar Murarishetti


🖥️ Part A – EC2 VM Setup & Connectivity
This week focused on working with two AWS EC2 virtual machines (VM1 and VM2) and practicing file transfers, instance modifications, and AWS automation via CloudFormation.

Steps Performed:
Connected to both VM1 and VM2 using MobXterm (a terminal for SSH and SFTP).

Verified network details using:

bash
ip -a
This ensured both instances were online and had proper network configurations.

📂 File Transfer Operations
1. Local → VM1
Transferred files from the local system to VM1’s /tmp directory.

Verified file presence before and after transfer using:

bash
ls -l /tmp

2. Local → VM2
Transferred files from local system to VM2’s /tmp directory in the same way.

3. VM → AWS EC2
From a VM session, uploaded files directly to another EC2 instance’s /tmp folder using scp:

bash
scp filename.txt ec2-user@<EC2-IP>:/tmp

4. VM2 → VM1
Sent file txt2 from VM2 to VM1’s /tmp directory using:

bash
scp txt2 ec2-user@<VM1-IP>:/tmp

Confirmed the transfer was successful.

⚙️ Part 3 – Instance Type Modification
Used AWS Console to change EC2 instance type to:
t3.2xlarge

This step was to increase CPU and memory resources for better performance.

💾 Part 4 – EBS Volume Management
Modified an existing EBS volume from the AWS console.

On VM2, verified attached volumes using:
bash
lsblk

Identified an extra volume that was not in use, detached it, and then deleted it to save costs.

☁️ Part 5 – AWS CloudFormation Automation
Actions Performed:
Created a new EC2 instance using CloudFormation stack (cloudformation2).

Validated successful deployment by checking running instances.

Deleted all resources created by the stack.

Stopped all other running instances after testing to avoid extra billing.

📌 Key Takeaways & Learnings
Remote Access & File Transfers:

Learned to use MobXterm for secure SSH access and file transfers.

Practiced moving files between local ↔ EC2 and EC2 ↔ EC2 using scp.

Instance Management:

Understood the impact of changing instance types for scaling applications.

Learned when and why to increase CPU/memory capacity.

EBS Storage Operations:

Learned how to list, modify, detach, and delete volumes.

Understood cost implications of unused EBS storage.

Infrastructure as Code (IaC) with CloudFormation:

Created, managed, and deleted AWS resources via templates.

Saw how automation reduces manual configuration errors.

📁Structure for GitHub

Week-5/
├── File_Transfer_Commands.txt
├── Instance_Modification_Notes.txt
├── Volume_Management_Notes.txt
├── CloudFormation_Deployment.txt
├── Screenshots/
│   ├── vm1_ip_a.png
│   ├── vm2_ip_a.png
│   ├── transfer_local_vm1.png
│   ├── transfer_vm2_vm1.png
│   ├── instance_type_change.png
│   ├── lsblk_volumes.png
│   └── cloudformation_created.png
└── README.md
