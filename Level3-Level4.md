## Level Goal:

The goal of this level was for me to retrieve the password which was stored in a hidden file in a directory on the server.

### Commands Used:

```bash
1. ssh bandit3@bandit.labs.overthewire.org -p 2220
2. ls
3. cd inhere
4. ls -l
5. cat total (cat: total: No such file or directory)
6. ls -a
7. cat ...Hiding-From-You (Password Retrieved)
8. exit
```

### Reflection:

This level taught me that Linux hides certain files by naming convention. These files have filenames that start with a period {.filename}, and are usually files that store important information such as system configurations.
