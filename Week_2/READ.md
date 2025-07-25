Week 2 - Bitnami VM Setup, Hadoop Configuration and File Operations
Student: Sai Kumar Murarishetti 

Tasks Completed:

Bitnami VM Setup & Configuration:
Download & Setup:

Downloaded the Bitnami image, renamed it as Sai-bitnami-fall23 for easy identification.
Allocated 4 GB RAM and 2 CPUs to the Bitnami virtual machine (VM).
Added two network adapters to ensure proper network functionality in the VM.

Starting the VM:
Successfully started the Bitnami VM and checked the network settings by running the command ip a to verify the VM’s IP address.

Firewall and SSH Configuration:
Disabling the Firewall:
Disabled the firewall on the VM to allow unhindered communication between the local system and the VM.

Enabling SSH:
Initially encountered an error while attempting to connect using Mobaxterm.
Enabled SSH on the VM and confirmed the connection was successful by checking the Mobaxterm error status which changed from error to authentication confirming that SSH was active.

Hadoop Setup and File Operations:

🔹 Part 1: HDFS Operations

Folder Creation & File Management:
Created a new HDFS folder for storing test files.
Created sample test files for upload and used the ls command to display the folder contents.

File Copying and Viewing:
Copied files to the tmp folder in HDFS and viewed the file contents using the cat command.

Removing Files from HDFS:
Performed file removal from HDFS to practice basic file management operations.

🔹 Part 2: Airline Data File Operations

Airline Data Upload:

Downloaded the September 2012 Airline data, renamed it and uploaded it to the server.
Ran the head command to preview the contents of the uploaded file.

Block Size Configuration:
Set the block size for the data file before uploading, ensuring optimal data storage and retrieval.

Replication Factor & Blocks Management:
Set the replication factor for the large data file stored in HDFS to 1 for testing.
The file required 10 blocks to store the entire data (based on 2MB block size and 18MB file size).

File System Check:
Ran the HDFS fsck command to verify the health and consistency of the file system, ensuring the file was properly replicated and distributed across blocks.

Key Insights & Learnings:
Replication Factor: Ensuring appropriate replication (set to 1 for the test) is critical to maintaining data availability and fault tolerance in HDFS.
Block Size: Adjusting block size ensures efficient storage, with a 2MB block size chosen for optimal performance in this case.
HDFS Commands: Familiarized with key Hadoop commands like hdfs dfs -ls, hdfs dfs -cat and hdfs fsck for file management and system checks.
