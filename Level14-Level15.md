## Level Goal:

The goal of this level was for me to retrieve the password which was stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level,there is no password, only a private SSH key that can be used to log into the next level.

### Commands Used:

```bash
1. ssh bandit14@bandit.labs.overthewire.org -p 2220
2. ls
3. man openssl
4. exit
5. openssl s_client -connect localhost:30000               (Error)
6. ssh bandit14@bandit.labs.overthewire.org -p 2220
7. man s_client
8. man telnet
9. man nc
10. nmap -p 30000 –sV localhost                            (30000/tcp open ndmps?)
11. nc localhost 30000                                     (Password Retrieved)
12. exit
```

### Notes:

This level introduced basic network communications through the use of the network utility "nc"(netcat) and enabled me to retrieve the password by submitting a payload on the listener port.
