## Level Goal:

The goal of this level was for me to retrieve the password which was stored in an unspecified location on the server and was owned by user bandit7, owned by group bandit6 and 33 bytes in size.

### Commands Used:

```bash
1. ssh bandit6@bandit.labs.overthewire.org -p 2220
2. ls –al
3. pwd
4. cd ..
5. find . -type f -size 33c                                     (Permission Denied)
6. cd bandit7
7. ls -al
8. cd ../bandit6
9. find . -type f -user bandit7 -size 33c                       (Permission Denied)
10. find . -type f -group bandit6 -size 33c                     (Permission Denied)
11. find . -type f -user bandit7 -group bandit6 -size 33c       (Permission Denied)
12. man find
13. find -type f -user bandit7 -group bandit6 -size 33c         (No Return)
14. find / -type f -user bandit7 -group bandit6 -size 33c
15. cat /var/lib/dpkg/info/bandit7.password                     (Password Retrieved)
16. exit
```

### Reflection:

This level introduced me to Linux file ownership and permissions, by allowing me to read a file owned by another user even when not authenticated as them. Because my authenticated user has Group ownership of the file, read permissions were extended to me. Here I learnt that I do not need to be explicitly authenticated as a specific user to access their files.
