## Level Goal:

The goal of this level was for me to retrieve the password which was stored readme in the homedirectory; the .bashrc file had been modified to log my user out when I log in with SSH.

### Commands Used:

```bash
1. ssh bandit18@bandit.labs.overthewire.org -p 2220                  (ByeBye !)
2. ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme       (Password Retrieved
```

### Reflection:

This level introduced non-interactive command execution by allowing me to pass the "cat readme" command directly into the ssh connection string, enabling me to bypass the .bashrc configuration file that was manipulated to log me out and retrieve the password.
