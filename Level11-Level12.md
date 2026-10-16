## Level Goal:

The goal of this level was for me to retrieve the password which was stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

### Commands Used:

```bash
1. ssh bandit11@bandit.labs.overthewire.org -p 2220
2. ls
3. cat data.txt
4. man tr
5. man xxd
6. tr ‘A-Za-z' ‘N-ZA-Mn-za-m' data.txt (tr: extra operand 'data.txt')
7. tr ‘A-Za-z' ‘N-ZA-Mn-za-m' < data.txt (Password Retrieved)
8. exit
```

### Reflection:

This level reinforced cryptography through ROT13 encryption, which is a symmetric encryption algorithm that encrypts data by replacing each character in a string with a character 13 places ahead of it. Here the password was retrieved by using a character mapping utility "tr" which enabled me to decode the algorithm translate the characters rotated 13 places to their original place to retrieve the password.
