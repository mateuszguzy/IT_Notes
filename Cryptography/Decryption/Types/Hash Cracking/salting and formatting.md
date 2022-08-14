


  
Regarding the used tool all of them has the same format. A file with the hash in it has each hash separated by a new line, like:  
  
<hash 1>  
  
<hash 2>  
  
<hash 3>  
  
  
**Salts**, ale typically appended onto the hash with a colonand the salt. Files with salted hashes still follow the same convention:◇   
  
<hash1>:<salt>  
  
<hash2>:<salt>  
  
<hash3>:<salt>  
  
  
Salt is a random data used as additional input to a one-way function that hashes the data. Salts are used to safeguard passwords in storage.