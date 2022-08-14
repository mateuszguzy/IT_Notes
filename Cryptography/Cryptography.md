


  
Basic terms:  
• **ciphertext** - result of encrypting a plaintext - encypted data.   
• **cipher** - encrypting or decrypting method. Moder ciphers are cryptographic.  
• **plaintext** - data before encryption, often text but not always. Could be a photo or other file  
• **encryption** - transforming data into ciphertext, using a cipher  
• **encoding** - NOT a form of encryption, just a form of data representation like base64. Immediately reversible.  
• **key** - information needed to decrypt the ciphertext and obtain the plaintext  
• **passphrase** -separate to the key, similiar to password, used to protect a key  
• **asymetric enryption** - uses different keys to encrypt and decrypt  
• **symmetric encryption** - uses the same key to encrypt and decrypt  
• **brute force** - password cracking method which tries every different password or every different key  
• **cryptoanalysis** - attacking cryptography by finding a weakness in the underlying maths  
• **Alice and Bob** - represent two people who want to connect (A and B).   
  
  
Math behind cryptography  
   
Most important math operatot coming along with cryptography is Modulo operator ( % ). It's used while searching for reminder.   
◇ 16 % 5 = 3 with reminder 1  
  
  
Establihing keys using asymetric cryptography  
 ◇ It's common way i.e. in HTTPS to use asymetric cryptography to exchange keys for symmetric encryption. Asymmetric tends to be slower so fro HTTPS symmetric is better. Best explained in metaphor:  
◇   
◇ Alice and Bob want to exchange mail in secret code, but firstly they need to establish it.   
◇   
◇ ▪ Alice send Bob a lock, which only Alice has key to  
▪ Bob locks secret code in indestructible box and sends to Alice  
▪ Alice recieves box and opens lock with her key  
▪ Bob and Alice know a secret code to they can now exchange mail with it's use  
  
  
  
◇   
  
Diffie Hellman key exchange  
 ◇ Establishing secure symmetric keys securely and without using asymmetric cryptograhpy.  
◇   
◇ ▪ Alice and Bob both have generated secrets - **A**and **B**  
▪ They also have common material that is public - **C**  
▪ Alice and Bob both combine their secrets with common material and form **AC**and **BC**  
▪ They send each other these and combine that with their secrets to form two idential keys, both **ABC**  
  
  
◇   
◇ Important assumption is that combined secret/material is impossible to separate, and order that they are combined doesn't matter.  
  
