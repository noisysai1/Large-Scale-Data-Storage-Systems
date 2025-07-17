Week 1  - VirtualBox & CentOS VMs Setup

Student Name: Sai Kumar Murarishetti
University ID: 30079224

🔹 Objective:
To install and configure CentOS 7 virtual machines using Oracle VirtualBox, understand VM cloning techniques, perform basic Linux commands and explore VirtualBox features related to VM management.

🔹 Tasks Performed:

Virtual Machine Setup:
Verified Virtual Machine network connectivity via Control Panel.
Installed CentOS 7 as the base operating system in VirtualBox.

VM Cloning:
Created multiple clones of the base VM:
VM1: Configured with 1.5 GB RAM and 1 CPU.
VM2 (Full Clone): Configured with 2 GB RAM and 1 CPU.
VM3 (Linked Clone): Configured with 0.5 GB RAM and 1 CPU.


Basic Linux Operations in VM1:
Installed curl for data transfer tasks.


Executed:
free -h command to monitor memory usage.
ping command to check network connectivity.
echo command for basic output.
Created text files and transferred them to VM2 and VM3 using SCP commands.

VirtualBox Concepts Explored:

VM Start Options:

Normal Mode – GUI-based operation.
Headless Mode – CLI operation, no GUI.
Detachable Mode – GUI can run independently.
Export Appliance: Packaging VM and settings for sharing or backup.

Snapshots:
Benefits: Quick backups, versioning, easy rollback.
Drawbacks: High storage use, performance impact over time.

System Monitoring:

Identified attached disks in VM2 using terminal commands.
Checked VM folder sizes to compare disk space usage among full and linked clones.

Networking Insight:

Learned the significance of 127.0.0.1 (loopback address) and its role in self-communication testing.


🔹 Key Learnings:

Setting up multiple CentOS VMs.
Using Full Clone vs. Linked Clone.
Running basic Linux commands across multiple VMs.
Understanding the utility of snapshots, export appliance, and various VM startup modes in VirtualBox.
Importance of localhost IP in networking.
