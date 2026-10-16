## Level Goal:

The goal of this level was for me to retrieve the password by submitting the password of the current level to a port on localhost in the range 31000 to 32000 that speaks SSL/TLS.

### Commands Used:

```bash
1. ssh bandit16@bandit.labs.overthewire.org -p 2220
2. man openssl
3. man s_client
3. man nmap
4. nmap -p 31000-32000 127.0.0.1 -T4 -sV
5. openssl s_client -connect localhost:31518
6. openssl s_client -connect localhost:31790           (Private Key Retrieved)
7. exit
8. nano private.key
9. chmod 600 private.key
10. ssh -i private.key bandit17@bandit.labs.overthewire.org -p 2220
11. cat /etc/bandit_pass/bandit17                      (Password Retrieved)
12. exit
```

### Reflection:

This level reinforced secure network communication through tool "openssl" tool, key based authentication, and more importantly introduced port scanning through the use of the network mapping tool "nmap", which all enabled me to retrieve the password by submitting a payload on the appropriate SSL/TLS listener port.
