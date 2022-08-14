


  
**RSA** (Rivest Shamir Adleman) is based on mathematically difficult problem of working out the factors of a large numbers. I.e. it's quick to multiply two prime numbers - 17\*23 = 391. But it's challenging to work out what two prime numbers multiply together to make 14351.   
  
Math behind RSA often comes up with CTF's, requiring to calculate variable or break some encryption. To help with that, some tools are available (rsatool or RsaCtfTool).  
  
Key variables needed to know in case of RSA in CTF are:  
• **p** and **q** - large prime numbers   
• **n** - product of p and q  
• **n** and **e** - public key  
• **n** and **d** - private key  
• **m** - represent the message (plaintext)  
• **c** - represents the ciphertext  
  
  
  
  
  
  
  
