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

## Supporting Screenshots
<img width="1363" height="409" alt="image" src="https://github.com/user-attachments/assets/de34c5be-bd9a-4d02-a214-5bfff1f2b853" />

**Screenshot 1-** Pfsense firewall rules creation for OPT1 DMZ.

<img width="852" height="649" alt="image" src="https://github.com/user-attachments/assets/53447fd4-6c98-4637-8c89-01bfa9ad6324" />

**Screenshot 2-** Using the command Nmap from Ubuntu to Windows.

<img width="1149" height="579" alt="image" src="https://github.com/user-attachments/assets/1ce48827-16c7-47a8-8e20-445faca859e7" />

**Screenshot 3-** Running Nmap on windows to itself proving port 80 is open.

<img width="1459" height="808" alt="image" src="https://github.com/user-attachments/assets/bbfbf736-b7d5-4afe-8abc-69383b72627f" />

**Screenshot 4-** Apache web verification.

## Lab 2 **Creating Secure Architectures**
Lab 2 [Link](https://napier.apporto.com/collaboration/dFoTwUibIvj18RHj94f64PJ8%2BE6YQL2xQ0VaVYnAdJIkRd%2B0w7KfA%2FhZeSLanWcrhlJQSO6OH7IgHOLPQmwpp%2B4kXrCUPiu2x0%2B2jRnQMOKqmw7WJPhF921xHBjCGi6L7UxeOqjUtALaCx8HOlhyMtUa2NGJ%2F1VXPiHctgvxSsU%3D)
## Overview
In this exercise i continued to use the network architecture built in Lab 1, This lab introduced penetration testing methodologies using tools such as **Nmap**, **Hydra**, and **Metaspliot** and packet analysis using **Wireshark**.

## Key elements of learning
* **Anlysis of network traffic:** Using Wireshark to analyze network traffic as well as extract telnet plaintext credentials and inspect encrypted SSH payloads.
*  **Reconnaissance:** Executed HTTP banner grabbing via telnet to identify server versions and operating system versions using the command telnet 192.168.10.7 80.
*  **Service expliotation:** utilized hydra to automate credential cracking against FTP service on TCP port 21.

## Key difficulties
I didn't ran into much difficulties except remembering that i have to set the Metasploitable and Kali hosts IP address again and make sure that the network adaptor on both host machine is up and that the default gateway is set to the right gateway as well as the name server is set to 8.8.8.8.
## Supporting Screenshots

<img width="1554" height="1086" alt="image" src="https://github.com/user-attachments/assets/1c231f96-5c1e-494b-99bd-e068aecbcaec" />

**Screenshot 1-** extracting telnet plaintext credentials "username:msfadmin password:napier123" using Wireshark TCP stream.

<img width="1499" height="462" alt="image" src="https://github.com/user-attachments/assets/e61239a3-c508-4154-89ab-ec1bcd0746f6" />

**Screenshot 2-** Successfully bypassing a host key type negotiation error to log in to metasploitable machine via SSH. 

<img width="1424" height="1067" alt="image" src="https://github.com/user-attachments/assets/aff9d577-aadc-4a33-b26d-68ca61bf34da" />

**Screenshot 3-** Viewing a TCP stream in Wireshark that captures the SSH protocol handshake and the encrypted session payload between client and server.

<img width="1088" height="516" alt="image" src="https://github.com/user-attachments/assets/7c472714-26ee-4e8b-8f21-e35ab0be42fe" />

**Screenshot 4-** Executing Hydra brute-force attack against FTP service 192.168.11.9 using a custom user and password lists.

<img width="1121" height="805" alt="image" src="https://github.com/user-attachments/assets/46cd6bef-f628-4508-9463-08ca46f15bfe" />

**Screenshot 5-** Utilizing the "auxiliary/scanner/smb/smb_enumshares" in Metasploit to authenticate and successfully discover active smb shares on the target host 192.168.11.7.

## Lab 3 **AWS Security and Server Infrastrcuture**
Lab 3 Link [Windows](http://52.55.247.89/) [Ubuntu](http://52.55.247.89/)
## Overview
Using AWS academy learner lab i have been instructed to deploy and configured two servers which are Ubuntu a linux based server and windows 2022 server. This also includes configuring security groups as well as firewall which are host based like windows defender and AWS rules services "ICMP, HTTP, RDP, and SSH" the lab also conducted modifying instance hardware specifications using the AWS cli and as well as using python for automating boto3 scripts. 

## Key elements of learning
During this exercise, Ubuntu server and Windows server 2022 were deployed using the AWS learner's lab EC2 instances as well as configuring security groups to strictly control SSH, HTTP, HTTPS, and RDP traffic. A secondary Linux admin user were created and SSH configuration file was modified to permit password-based authentication alongside the default public keys. Forensic analysis was conducted by auditing Apache and Windows IIS logs to extract clients IPs, HTTP status codes and user agent details. Lastly, the AWS CLI was utilized to manage instance states and scale hardware types and python scripts "Boto3 library" to develop automate key pair generation and EC2 lifecycle.

## Key difficulties
