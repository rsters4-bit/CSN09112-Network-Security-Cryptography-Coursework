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
