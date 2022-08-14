


  
JTR mode to cracking hashes with informations provided in username.   
  
Whole mode rely on word mangling, like in example below.  
• Username: Markus  
•   
• Possible password:  
•   
• ◇ Markus1, Markus2, Markus3 (etc.)  
◇ MArkus, MARkus, MARKus (etc.)  
◇ Markus!, Markus$, Markus\* (etc.)  
◇   
  
  
  
JTR has own dictionary based on information that is has been fed and uses a set of rules called "mangling rules" which define how much it can mutate the word it started with to generate a wordlist based off of relevant factors for the target.  
  
It also can work with GECOS fields. JTR can take informations stored in those fields such as full name or home directory name to add to wordlist it generates when single cracking shadow file.  
  
Syntax:  
  
![461-1.png](461-1.png)  
  
  
  
◇ ▪   
  
  
  
