# Population-Health-Surveillance-Architecture
A project focused on creating virtual healthcare systems, setting up electronic health records, simulating data with synthetic sources, and making sure everything works together using OpenEMR, Synthea, and HAPI-FHIR.
# Architecture Development Part 1: Virtual Machine Configuration/Testing 
I set up a network with five virtual machines: four for hospitals and one for a Health Information Exchange (HIE). Each hospital VM runs an operating system that works with OpenEMR, and the HIE VM runs an OS that works with HAPI-FHIR. I checked the connections by pinging each hospital from the HIE VM. The table confirms the OS compatibility and shows the network is working.
