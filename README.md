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
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/86d1541665a73012fea25060042d2e75661104bc/Aspirus%20Ubuntu.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/1b8a10306894dd12b269882a4e0449df4da86361/BCMH.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/b03da736e6a04cf3e992ae0117cfa70644abdf45/MGH.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/b03da736e6a04cf3e992ae0117cfa70644abdf45/Portage%20Hospital.png)

# Architecture Development Part 3: Generation of Synthea Patient and Syndromic Surveillance Data for Hospital EHRs to Simulate Disease Outbreak
Steps
Installing Synthea 
Download the latest version of Synthea from the official GitHub repository
Create a directory for Synthea and move the JAR file
Generating COVID Simulation Messages in the synthea directory.

Below are Evidence of Synthea Patient Generation and Table showing number of Patients.

![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/260ef923b954882c808b1cc9ab51c1bb55d2180d/A3.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/260ef923b954882c808b1cc9ab51c1bb55d2180d/PORTAGE%20HOSPITAL%20SYNTHEA-3.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/260ef923b954882c808b1cc9ab51c1bb55d2180d/MGH%20SYNTHEA-3.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/260ef923b954882c808b1cc9ab51c1bb55d2180d/BCMH%20SYNTHEA-3.png)
![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/260ef923b954882c808b1cc9ab51c1bb55d2180d/ASPIRUS%20UBUNTU%20SYNTHEA-3.png)


# Architecture Development Part 4: Installation and Configuration of Hapi-FHIR Server
Steps
1. Log in to the UPHIE VM
2. Verify Docker Installation
3. Pull the HAPI FHIR Docker Image
4. Configure HAPI FHIR
5. Deploy the HAPI FHIR Container
6. Verify Deployment
7. Access the HAPI FHIR Portal
8. Manage the Container

Below are visuals of installation and configuration of Hapi-FHIR Server





   

