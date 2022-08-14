


  
**john** - advanced and simple hash cracking tool.  
  
Syntax:  
  
 john [options] [file\_path]  
  
• [file\_path] indicates full path to hash file wanting to crack, but if in the same folder, no path needed, just the file name.  
  
  
Automatic cracking:  
  
 john --wordlist=[wordlist\_path] [file\_path]  
  
JTR has implemented automated tool for cracking in case hash format is not known. It's not best solution because it can be faulty, but it's a good start if no data is known.   
  
Format-specific cracking  
  
When hash format is known JTR can be set to work with specific hashes only.  
  
 john --format=[format] --wordlist=[wordlist\_path] [file\_path]  
  
Example:  
  
 john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash\_to\_crack.txt  
  
  
When using JTR for cracking standard type hashes like md5, prefix " **raw-**" is needed.   
  
Useful is also to list all formats JTR is working with and grep wanting keyword:  
  
![459-1.png](459-1.png)  
  
Shadow hashes  
  
To crack shadows hashes, JTR needs two files combined togehter to "understand" the data. It's the shadow file, and the passwd file. To do this, a built-in tool can be used.  
  
![459-2.png](459-2.png)  
  
After unshadowing created data can be stored in separate file, using syntax:  
unshadow local\_passwd local\_shadow > unshadowed.txt  
  
  
For unshadowing a whole files can be used, or just specific lines, syntax:  
FILE 1 - local\_passwd  
  
  
First line of file contains:◇   
root:x:0:0::/root:/bin/bash  
  
  
And  
FILE 2 - local\_shadow  
  
  
Second line of file contains:  
  
 root:$6$2nwjN454g.dv4HN/$m9Z/r2xVfweYVkrr.v5Ft8Ws3/YYksfNwq96UL1FX0OJjY1L6l.DS3KEVsZ9rOVLB/ldTeEL/OIhJZ4GMFMGA0:18576::::::  
  
Most of the time there is no need to provide special format, because unshadowed file is created strictly for JTR. But sometimes it's not enough.  
  
  
  
  
  
  
  
  
  
  
