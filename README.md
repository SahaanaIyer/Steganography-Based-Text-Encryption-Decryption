# Steganography-Based-Text-Encryption-Decryption
An encryption-decryption process using Steganography, AES, Vighnere and Diffie-Hellman Key Exchange  

Client Side - 

1. Generate Key Ka1 using Diffie Hellman Key Exchange 
2. Generate Key Ka2 using Diffie Hellman Key Exchange 
3. AES Encryption using Ka1 - Converting String into Bytes 
4. Convert Bytes into Hexadecimal 
5. Splitting Hexadecimal into v1 and v2 such that v1 contains first 10 alphabets and v2 contains all numerical digits followed by remaining alphabets 
6. Vighnere Encryption on v1 using Ka2 
7. Steganography Image Encryption on vighnere encrypted v1 
8. Send stego image, encrypted v2, positions array of initial characters to Server  
 
Server Side - 

1. Generate Key Kb1 using Diffie Hellman Key Exchange 
2. Generate Key Kb2 using Diffie Hellman Key Exchange 
3. Receive stego image, encrypted v2, positions array of initial characters from Client 
4. Steganography Image Decryption on vighnere encrypted v1 
5. Vighnere Decryption on v1 using Kb2 
6. Rejoining v1, v2 using their initial positions in Hexadecimal 
7. Converting Hexadecimal into Bytes 
8. AES Decryption using Kb1 - Converting Bytes into String
