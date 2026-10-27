## Lab 5 **Public key and Key exchange** 
## Overview
This lab demonstrates practical implementation of public key and key exchange using AWS KMS tools with Python scripting. the lab started with manual RSA encryption and decryption using AWS CLI before automating using "boto3" library. Then the lab progressed into verifying data integrity with digital signatures and ended with building a custom python script to handle symmetric AES encryption.

## Key elements of learning
* Utilizing and managing AWS KMS customer managed keys, including setting up aliases and understanding how strict usage policies work in practice.
* Converting Base64 ciphertext into readable binary and standard public key formats "DER/PEM" using terminal tools and OpenSSL.
* Writing Python automation with "boto3" library to interact with cloud cryptography services rather than relying on manual CLI commands.
* Implementing symmetric encryption using "cryptography.hazmat" library, handling PKCS7 data padding, and making scripts dynamic by parsing CLI arguments.
  
## Key difficulties
* Running into an "InvalidKeyUsageException" when trying to sign a document with an encryption key, providing that AWS KMS key usage is permanently locked at creation and requires a dedicated "SIGN_VERIFY" key for signatures.

## Supporting screenshots
<img width="652" height="556" alt="image" src="https://github.com/user-attachments/assets/38f718d8-8487-457a-875a-df5290090b25" />

**Screenshot 1-** Executing a Diffie-Hellmann key exchange within a kali linux python terminal.

<img width="757" height="281" alt="image" src="https://github.com/user-attachments/assets/3194297d-f253-40e6-9e43-d17fd4b8e12a" />

**Screenshot 2-** Using OpenSSL in kali terminal to extract RSA public key from private key as well as encrypt a text file and successfully decrypt the resulting binary data to reveal the message.

<img width="687" height="490" alt="image" src="https://github.com/user-attachments/assets/813b0299-67a6-440e-80a1-8e03d624be73" />

**Screenshot 3-** Generated a Certificate Signing Request "CSR" using OpenSSL followed by using a private key to create a self signed digital certificate "server.crt"

<img width="2409" height="390" alt="image" src="https://github.com/user-attachments/assets/f0ada33d-1a78-4b52-8685-68ff610816d4" />

**Screenshot 4-** Successfully encrypt a local text file using RSA. The generated Base64 ciphertext is then decoded into a binary format and decrypted back using AWS KMS.

<img width="2374" height="178" alt="image" src="https://github.com/user-attachments/assets/0930e6b4-5a2d-4893-9da8-5e0f9af55541" />

**Screenshot 5-** Using a Python script in AWS terminal to intialize an AWS KMS client using a specific key ID. The program successfully encrypts a plaintext message into a Base64 encoded ciphertext string and then decrypts it back into a readable format.

<img width="2423" height="299" alt="image" src="https://github.com/user-attachments/assets/5389852f-d249-4e7f-9978-155aef405ecd" />

**Screenshot 6-** By using AWS CLI digital signature for a local text file was successfully generated using "SIGN_VERIFY" KMS key. The Base64 output was decoded into binary signature file and authenticated via "aws kms verify" command confirming that the signature is valid.

<img width="1615" height="497" alt="image" src="https://github.com/user-attachments/assets/c4ba1659-9f3d-4da0-bdd7-2689e8a4d259" />

**Screenshot 7-** Retrieve a public key from AWS KMS using AWS CLI and OpenSSL and converting it from DER to PEM format and display the key contents. The process also includes verifying a digital signature "1.sig" against the orginal text file "1.txt" which results a "Verified OK" confirmation.

<img width="1312" height="756" alt="image" src="https://github.com/user-attachments/assets/ad223c0e-42ef-41a5-99af-b2e1ac43d1ca" />

**Screenshot 8-** Created a python script using "pycryptodome" and modified it using CLI arguments to perform AES symmetric encryption. The output script successfully demonstrate padding, encrypting, and decrypting vatrious message and key combinations to generate specific ciphertext.

