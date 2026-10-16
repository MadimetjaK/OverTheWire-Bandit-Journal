## Level Goal:

The goal of this level was for me to retrieve the password  by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

### Commands Used:

```bash
1. ssh bandit15@bandit.labs.overthewire.org -p 2220
2. openssl s_client -connect localhost:30001           (Password Retrieved)
3. exit
```

### Reflection:

This level introduced secure network communication through the use of the network tool "openssl" and enabled me to retrieve the password by submitting a payload on the listener port. A point of interest here was the difference between netcat and openssl, where netcat is a network communications tool that passes data in plaintext, and openssl encrypts the data it passes by wrapping it in TLS/SSL to prevent anybody from reading the data if intercepted.
