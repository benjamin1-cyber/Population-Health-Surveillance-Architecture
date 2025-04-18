# Public-Health-Surveillance-Architecture
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

VM Configuration
1.	Deploy from Template
2.	Configure Hardware
3.	Network Setup
4.	Guest OS Configuration (Ubuntu)
5.	Repeat for Additional VMs
   
Below is evidence of VM created

![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/cbeb0e94cb21b0a5cf18eeb4ed38acf1aadd7f9f/A2.png)

The table confirms the OS compatibility and shows the network is working.

![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/e034b8018517ac182bec7493cafbd243dab48191/A1.png)


# Architecture Development Part 2: Installation, Configuration, and Security of OpenEMR
This Architecture focuses on setting up and configuring OpenEMR, an open-source electronic health record (EHR) system, across four virtual hospital environments as part of a simulated health information exchange architecture. OpenEMR is a powerful tool used globally to manage patient data, scheduling, billing, and clinical workflows, and it's especially valued for its flexibility and cost-effectiveness. As part of this hands-on experience, I will be installing OpenEMR (version 6.0.1) on separate virtual machines, configuring both its database and web server, and ensuring each instance is secure and accessible from its hospital VM. The goal is to gain a strong understanding of EHR components, security best practices, and the core modules that support digital healthcare operations. This work is a key step in building out my virtual hospital network and aligning it with real-world public health informatics practices.

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
This work is about learning how to generate synthetic patient and syndromic surveillance data using Synthea, a tool designed to create realistic, privacy-safe healthcare data. The main goal is to simulate a disease outbreak—like COVID-19—across a specific geographic area using synthetic patient records, allowing for more informed and timely public health decision-making. In this module, I will be using Synthea to generate patient data that mimics real-world scenarios, including demographics, conditions, and treatments. This experience is especially valuable for developing skills in public health research, outbreak modeling, and understanding the strengths and limitations of synthetic data. It helps me explore how surveillance systems can be tested and improved without using real patient records, which supports both privacy and innovation in healthcare analytics.
Steps
Install Synthea 
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
This architecture is about setting up and working with HAPI-FHIR, an open-source server that supports the FHIR standard—a modern framework for exchanging healthcare data across systems. I will be installing and configuring HAPI-FHIR within the HIE (UPHIE) virtual machine to enable secure, real-time sharing of health information between my virtual hospitals. This is a key step in building a connected public health surveillance system that supports early outbreak detection and coordinated responses. Through this module, I will get hands-on experience with FHIR concepts, troubleshoot server-related issues, and better understand how interoperability tools like HAPI-FHIR contribute to efficient public health data exchange and informed decision-making during disease outbreaks.

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

![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/51be6e498a08badfd4ba5aac9c21da86380c13b5/A4.png)


# Architecture Development Part 5: Interoperability- FHIR Data Exchange with HAPI-FHIR
This module focuses on using HAPI-FHIR to receive and process HL7 FHIR messages for public health surveillance, especially in the context of disease outbreaks like COVID-19. This set up HAPI-FHIR to accept standardized data from EHR systems and write custom scripts to extract key information—such as patient demographics, lab results, and clinical observations. This hands-on work will improve understanding on how real-time data exchange supports faster analysis of public health trends and more informed decisions for resource allocation and intervention strategies. Through this work, I gained practical experience in leveraging HAPI-FHIR’s capabilities to monitor and respond to public health challenges efficiently.

Steps for FHIR Data Exchange with HAPI FHIR and Postman
1. Install Postman
2. Access HAPI FHIR Swagger UI
3. Create a New Practitioner (POST Request) 
4. Search for Practitioners (GET Request)
5. Filtered Search
6. Update/Delete a Practitioner
7. Use HAPI FHIR Dashboard
8. Python REST API Example

Below is Visuals of the results

![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/fe013071b758bbf954e74e740846454dce8b8564/A4.png)


# Architecture Development Part 6: Aggregation and Visualization of
Data for Disease Outbreak Surveillance
This architecture is all about learning how to aggregate and visualize FHIR-based patient data—originally generated with Synthea in .json format—from four virtual hospitals to support public health analytics and communication. I will be writing a Python script to combine relevant data from each hospital, then converting it into a format that can be used to create an interactive Disease Outbreak Dashboard in Google Looker Studio. This dashboard will help communicate key insights like COVID-19 case trends by location, supporting real-time decisions by healthcare professionals, public health agencies, and even informing the general public. Through this hands-on task, I will deepen my understanding of how FHIR data is structured, how to work with it programmatically, and how data visualization tools can drive awareness, preparedness, and policy-making in public health.

Aggregate Data Using Python
1.	Understand FHIR Data Structure
2.	Use or Modify the Sample Python Script
3.	Format and Export to CSV
4.	Add Comments to Your Script

Visualize Data in Google Looker Studio
1.	Upload Your CSV File
2.	Create Visualizations
3.	Set Auto-Refresh
4.	Title & Share the Dashboard

Below is the visuals of results

![](https://github.com/benjamin1-cyber/Population-Health-Surveillance-Architecture/blob/3f8cc62135f52a167e2cc977ab7a4c4d1bca2621/A6.png)









   

