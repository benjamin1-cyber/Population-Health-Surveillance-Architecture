# Population-Health-Surveillance-Architecture
A project focused on creating virtual healthcare systems, setting up electronic health records, simulating data with synthetic sources, and making sure everything works together using OpenEMR, Synthea, and HAPI-FHIR.
# Architecture Development Part 1: Virtual Machine Configuration/Testing 
I set up a network with five virtual machines: four for hospitals and one for a Health Information Exchange (HIE). Each hospital VM runs an operating system that works with OpenEMR, and the HIE VM runs an OS that works with HAPI-FHIR. I checked the connections by pinging each hospital from the HIE VM.
# steps to connect to Cluster and VM configuration
Virtual Cluster Access
1.	Set Up MTU-VPN
2.	Access the Cluster via Browser
3.	Navigate to Your Class Folder
4.	Locate Templates
5.	Completion-You are now connected and ready to deploy VMs
________________________________________
VM Configuration
1.	Deploy from Template
2.	Configure Hardware
3.	Network Setup
4.	Guest OS Configuration (Ubuntu)
5.	Repeat for Additional VMs
________________________________________
Below is evidence of VM created
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/cbeb0e94cb21b0a5cf18eeb4ed38acf1aadd7f9f/A2.png)

The table confirms the OS compatibility and shows the network is working.
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/e034b8018517ac182bec7493cafbd243dab48191/A1.png)

# Architecture Development Part 2: Installation, Configuration, and Security of OpenEMR
________________________________________
Steps for OpenEMR Installation Sequence Commands
1.	Update Ubuntu
2.	Install LAMP Stack
3.	Create MySQL Database for OpenEMR
4.	Download & Install OpenEMR
5.	Configure Apache
6.	Complete Web-Based Setup

 Steps in Securing OpenEMR on Virtual Machine using Ubuntu Server
Steps:
1.	Update Ubuntu
2.	Enable Automatic Security Updates
3.	Configure Firewall (UFW)
4.	Secure Apache
5.	Use Strong Passwords
6.	Set Up Backups
7.	Keep OpenEMR Updated

Below are evidence of Steps above
![](
   

