## Level Goal:

The goal of this level was for me to retrieve the password which was human-readable, non executable and 1033 byes in size, in the inhere directory.

### Commands Used:

```bash
1. ssh bandit5@bandit.labs.overthewire.org -p 2220
2. ls
3. cd inhere
4. ls
5. ls ./maybehere00
6. ls -al ./maybehere00
7. find . -type f -size 1033c       (./maybehere07/.file2)
8. cat ./maybehere07/.file2         (Password Retrieved)
9. exit
```

### Reflection:

This level introduced me to Linux filesystem traversal through the "find" command, which I used to identify the file specified properties to retrieve the password. I learnt that the find tool allows me to find any file within the directory tree by evaluating the external metadata of all files for the one that matches the specified properties.
