# CSN09112-Network-Security-Cryptography-Coursework
**Name:** Steven Baruc

**Matriculation Number:** 40772308

---

## Introduction-Overview 
This repository documents my coursework and lab progress for CSN09112 Network Security & Cryptography. it includes direct links to each completed labs, overviews of the exercises, key concepts learned, and reflections on the technical challenges encountered throughout the semester.

## Lab 1 **Virtualised Infrastructures**
Lab 1
[Link](https://napier.apporto.com/collaboration/dFoTwUibIvj18RHj94f64PJ8%2BE6YQL2xQ0VaVYnAdJIkRd%2B0w7KfA%2FhZeSLanWcrc7gV52CRUbHOY2U6MWw06e4kXrCUPiu2x0%2B2jRnQMOKqmw7WJPhF921xHBjCGi6LExxC5YoaxlNf%2F2lxbURhwtUa2NGJ%2F1VXPiHctgvxSsU%3D)
## Overview
In this lab we were task on setting up and configuring a multi subnet network environment. The goal was to build a segmented layout using a central firewall to isolate different zones instead of having every machine sit on one flat network.

<img width="1810" height="981" alt="image" src="https://github.com/user-attachments/assets/87524a49-be21-46c4-9b8d-fcfcdd0a300b" />

## Key elements of learning
* **Firewall Rule creation:** Configured stateful rules and access control lists (ACLs) on the central firewall (pfsense) to restrict inter-zone communication and control traffic entering and leaving the DMZ.
*  **Service Access Control:** Allowed inbound TCP port 80 (HTTP) and port 443 (HTTPS) from the public network into DMZ to simulate hosting accessible web applications without exposing other internal ports.
* **Testing and verification:** Checked that the firewall was behaving as intended using tools like **ping** and **nmap** to confirm that permitted ports were open and restricted traffic was blocked.
## Key difficulties
* **Windows 7 Virtual Network Adapter Detection:** The main practical challenge during setup was that the windows 7 virtual machine failed to detect its virtual network adapter on boot, leaving the system with no usable interface. because the OS lacked built in driver support for the virtualized device, i opened the VM node properties and updated the adapter type to **VMware Paravirtualized Ethernet v3 (vmxnet3)**. Once reconfigured with the compatible virtual driver, the interface initialized properly in Windows, allowing me to assign the static IP and proceed with gateway connectivity testing.

#Supporting Screenshots#
<img width="1363" height="409" alt="image" src="https://github.com/user-attachments/assets/de34c5be-bd9a-4d02-a214-5bfff1f2b853" />

**Screenshot 1-** Pfsense firewall rules creation for OPT1 DMZ

## Lab 2 **Creating Secure Architectures**
Lab 2 [Link](https://napier.apporto.com/collaboration/dFoTwUibIvj18RHj94f64PJ8%2BE6YQL2xQ0VaVYnAdJIkRd%2B0w7KfA%2FhZeSLanWcrhlJQSO6OH7IgHOLPQmwpp%2B4kXrCUPiu2x0%2B2jRnQMOKqmw7WJPhF921xHBjCGi6L7UxeOqjUtALaCx8HOlhyMtUa2NGJ%2F1VXPiHctgvxSsU%3D)
## Overview
In this exercise i continued to use the network architecture built in Lab 1, This lab introduced penetration testing methodologies using tools such as **Nmap**, **Hydra**, and **Metaspliot** and packet analysis using **Wireshark**.

## Key elements of learning
# ##
## Key difficulties

## Lab 3 **AWS Security and Server Infrastrcuture**
Lab 3 Link [Windows](http://52.55.247.89/) [Ubuntu](http://52.55.247.89/)
## Overview
## Key elements of learning
## Key difficulties
