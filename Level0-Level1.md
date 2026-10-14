### Level Goal:

The goal of this level was for me to log into the game using SSH. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### Commands Used:

```bash
    1. ssh bandit0@bandit.labs.overthewire.org -p 2220
    2. ls
    3. cat readme     (Password Retrieved)
    4. exit
```

### Reflection:

The level introduced simple directory enumeration through the "ls" command and file reading with the "cat" command. The use of port 2220 for the ssh connection instead of the standard port 22 also taught me that protocols are agnostic of port numbers and services such as ssh can be instructed to bind to any unused port, something I was not aware of.  
