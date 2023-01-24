#common_attacks 


# Password files
Password File contains password hashes for users passwords. It is publicly accessible, but SHOULD NOT contain hashes. If so, can be brute forced. 
Good practice is to have a seperate file for password hashes - a shadow password file. 

![[Hashing]]


# Types of attacks

## Brute force attacks
Try all possibilities. Only effective against short passwords.

## Dictionary attacks
Try all the words in the English (or other) language first.

## Hybrid attacks
Add variations to tries. I.e. numbers at the end.

## Rainbow table attack
Precomputes hashes.


# Password cracking software
[John the Ripper](https://www.openwall.com/john/)


# Beware
Storing passwords unencrypted. 
Must take care to use strong hashing and passwords should be only one piece of the puzzle. 