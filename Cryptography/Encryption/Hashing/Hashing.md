Hash function is any function that can be used to assign any sized data an fixed-size value. Values returned by function are called i.e. hash values or **hashes**.   
  
Hashes are used to index a fixed-size table called **hash table**. Use of hash function to index a hash table is called **hashing**.  
  
Hash is a hexadecimal number which is a "sum up" of everything that file consists of. No matter how big the original file is, by constantly crushing it down a single number can be reached. It's like this file singature. That process **can never go backwards**.  
  
Simplest hash algorithm: (not a good one)  
3 + 1 + 4 + 1 + 5 + 9 = 23   
  
  
**Main requirements:**◇ speed - should be reasonably fast to calculate even biggest files, but also shouldn't be too quick becuase it means it's easy to break  
  
◇ avalanche effect - if file has changed even one bit, whole hash must be completely different  
◇ avoid hash collisions - situation occurs when two files have exactly the same hash  
  
  
  
  
Hash collisions can be achieved artificially, by manipulating the file. It's dangerous considering file security.  
