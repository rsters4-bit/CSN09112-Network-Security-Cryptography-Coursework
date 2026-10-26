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
