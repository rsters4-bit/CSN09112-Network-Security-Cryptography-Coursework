## Lab 4 **Symmetric Key and Hashing** 
## Overview
This lab demonstrates the use of symmetric key encryption, hashing, and password cracking. Using Kali Linux and AWS, encrypting and decrypting files was practiced using ciphers like AES-256 via OpenSSL CLI tool along with password integrity verification such as pbkdf2 and file hashes using md5. password cracking was also used such as john the ripper and hashcat to crack windows nt and md5. python script "python boto3" was used in AWS to autommate the encryption and decryption process. gocryptfs tool was also use to securely store private keys. 
## Key elements of learning
* Utilized John the Ripper to execute dictionary attacks against NT hashes by creating wordlists.
* Applied AWS key Management Service to securely encrypt and decrypt local files using symmetric keys.
* Converted ciphertext between Base64 and raw binary formats to secure data transmission and local decryption.
* implemented "gocryptfs" to create secure vaults that output files contents into unreadable cyphertext when unmounted from the file system.
## Key difficulties
One challenge that was encountered was the expired token in AWS CLI which took a little while troubleshooting. This was resolved by realizing on the previous lab that the token had to be copied from the "details" section next to the CLI dashboard and pasted into credentials file to be updated.
## Supporting screenshots
<img width="1365" height="505" alt="image" src="https://github.com/user-attachments/assets/00bb4f4c-f5b2-4742-ae59-adda94f78625" />

**Screenshot 1-** This screenshot shows a decryption of AES-256 ciphertext in OpenSSL by testing multiple keys until the correct password "paris" reveals the hidden message "hello"

<img width="1361" height="1095" alt="image" src="https://github.com/user-attachments/assets/82fc4412-0c4c-458a-ba66-c4996dd34cc5" />

**Screenshot 2-** Successfully executing Hashcat dictionary attack to crack four MD5 hashes, revealing the recovered plaintext passwords using a custom wordlist.

<img width="876" height="315" alt="image" src="https://github.com/user-attachments/assets/9dcbeca2-2140-44f2-b8db-17068fc58dff" />

**screenshot 3-** Utilising john the ripper to crack NT hashes, recovering passwords "aberdeen" and "dundee" using a custom dictionary wordlist.

<img width="1291" height="876" alt="image" src="https://github.com/user-attachments/assets/51aab7b6-c479-4821-b56f-b1d3ccedf27b" />

**Screenshot 4-** This screenshot shows encrypting and decrypting a file using AWS KMS after overcoming a "ExpiredTokenException" and resolved by correctly formatting and updating the " ~./aws/credentials" file to authenticate the session.

<img width="1674" height="626" alt="image" src="https://github.com/user-attachments/assets/1bd90f30-08aa-4a51-a227-9ee9d7fcb8b9" />

**Screenshot 5-** unmounting a "gocryptfs" vault and to confirm that the raw encrypted file is unreadable by displaying cyphertext demonstrating that the contents are secure when the vault is closed.

