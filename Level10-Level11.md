## Level Goal:

The goal of this level was for me to retrieve the password which was stored in the file data.txt, which contains base64 encoded data.

### Commands Used:

```bash
1. ssh bandit10@bandit.labs.overthewire.org -p 2220
2. ls
3. cat data.txt
4. man base64
5. base64 -d data.txt           (Password Retrieved)
6. exit
```

### Reflection:

This level introduced cryptography through data decoding using the command "base64 {-d}", which enabled me to decode the bas64 encoded text in the data.txt file to retrieve the password.
