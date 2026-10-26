## Lab 3 **AWS Security and Server Infrastrcuture**
Lab 3 Link [Windows](http://52.55.247.89/) [Ubuntu](http://52.55.247.89/)
## Overview
Using AWS academy learner lab i have been instructed to deploy and configured two servers which are Ubuntu a linux based server and windows 2022 server. This also includes configuring security groups as well as firewall which are host based like windows defender and AWS rules services "ICMP, HTTP, RDP, and SSH" the lab also conducted modifying instance hardware specifications using the AWS cli and as well as using python for automating boto3 scripts. 

## Key elements of learning
During this exercise, Ubuntu server and Windows server 2022 were deployed using the AWS learner's lab EC2 instances as well as configuring security groups to strictly control SSH, HTTP, HTTPS, and RDP traffic. A secondary Linux admin user were created and SSH configuration file was modified to permit password-based authentication alongside the default public keys. Forensic analysis was conducted by auditing Apache and Windows IIS logs to extract clients IPs, HTTP status codes and user agent details. Lastly, the AWS CLI was utilized to manage instance states and scale hardware types and python scripts "Boto3 library" to develop automate key pair generation and EC2 lifecycle.

## Key difficulties
My only challenging part is when i was trying to ping the RDP windows machine from my personal host machine, i was able to connect RDP from my host machine but unable to ping. I've done a bit of troubleshooting and found that in my inbound rules on my windows server instance ICMP source protocol was set to 0.0.0.0/32 instead of 0.0.0.0/0.

## Supporting Screenshots
<img width="2206" height="1051" alt="image" src="https://github.com/user-attachments/assets/f1593700-828e-4bf4-ae35-5973a6cd7f35" />

**Screenshot 1-** Validation for Windows server web page using VMware kali machine and a modification by creating the iisstart.html "Main web site", "Hello to you".

<img width="2201" height="614" alt="image" src="https://github.com/user-attachments/assets/7fa57d4b-2b59-48d9-9da4-92424765bf39" />

**Screenshot 2-** Validation for Linux Ubuntu server web page using VMware kali machine.

<img width="2070" height="1347" alt="image" src="https://github.com/user-attachments/assets/b3f49d05-ee28-424b-805d-ed97f1d2c200" />

**Screenshot 3-** ICMP verification of windows defender inbound rule "file and printer sharing ICMPv4-in).

<img width="929" height="367" alt="image" src="https://github.com/user-attachments/assets/0a15aaf1-1fb8-4b1a-b6c1-b74a506323bf" />

**Screenshot 4-** Successful ping request from Host machine to 13.221.192.173.

<img width="1965" height="918" alt="image" src="https://github.com/user-attachments/assets/e2074249-c449-4925-bdd0-cbcb13b0f137" />

**Screenshot 5-** Copying credentials from AWS cloud access into credentials file using nano, and permission changes to enable to execute the file creation.

<img width="2399" height="1030" alt="image" src="https://github.com/user-attachments/assets/88957666-c583-4384-b176-93157e51a57f" />

**Screenshot 6-** Creating a new instance using python script and copying an existing Ubuntu instance AMI ID into the script.

<img width="2017" height="684" alt="image" src="https://github.com/user-attachments/assets/0b9d34f5-ed65-4822-94ea-6fd7212b0b1f" />

**Screenshot 7-** Terminating the created instance using python script.
