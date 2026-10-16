## Level Goal:

The goal of this level was for me to gain access to the next level by using the setuid binary in the homedirectory and retrieving the stored in (/etc/bandit_pass).

### Commands Used:

```bash
1. ssh bandit18@bandit.labs.overthewire.org -p 2220
2. ls
3. bandit20-do                                         (bandit20-do: command not found)
4. ./bandit20-do                                       (Run a command as another user.)
5. ./bandit20-do cat /etc/bandit_pass/bandit20         (Password Retrieved)
6. exit
```

### Reflection:

This level introduced privilege escalation through the use of a special file permission called SUID (Set User ID), enabling me to run commands as another user even though I am not authenticated as them, and retrieve the password.
