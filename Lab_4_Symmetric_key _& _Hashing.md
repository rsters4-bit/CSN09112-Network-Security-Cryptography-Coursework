## Lab 4 **Symmetric Key and Hashing** Currently in progress
## Overview
This lab demonstrates the use of symmetric key encryption, hashing, and password cracking. Using Kali Linux and AWS, encrypting and decrypting files was practiced using ciphers like AES-256 via OpenSSL CLI tool along with password integrity verification such as pbkdf2 and file hashes using md5. password cracking was also used such as john the ripper and hashcat to crack windows nt and md5. python script "python boto3" was used in AWS to autommate the encryption and decryption process. gocryptfs tool was also use to securely store private keys. 
## Key elements of learning
## Key difficulties
## supporting screenshots
<img width="1365" height="505" alt="image" src="https://github.com/user-attachments/assets/00bb4f4c-f5b2-4742-ae59-adda94f78625" />

**Screenshot 1-** Successfully decrypted an AES-256 ciphertext in OpenSSL by testing multiple keys until the correct password "paris" reveals the hidden message "hello"

<img width="1361" height="1095" alt="image" src="https://github.com/user-attachments/assets/82fc4412-0c4c-458a-ba66-c4996dd34cc5" />

**Screenshot 2-** Successfully executing Hashcat dictionary attack to crack four MD5 hashes, revealing the recovered plaintext passwords using a custom wordlist.

<img width="876" height="315" alt="image" src="https://github.com/user-attachments/assets/9dcbeca2-2140-44f2-b8db-17068fc58dff" />

**screenshot 3-** Successfully used john the ripper to crack NT hashes, recovering passwords "aberdeen" and "dundee" using a custom dictionary wordlist.

