## Level Goal:

The goal of this level was for me to retrieve the password which was stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level,there is no password, only a private SSH key that can be used to log into the next level.

### Commands Used:

```bash
1. ssh bandit13@bandit.labs.overthewire.org -p 2220
2. ls
3. cat HINT
4. man ssh
5. man chmod
6. exit
7. ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220           (Warning: Identity file sshkey.private not accessible: No such file or directory.)
8. ssh bandit13@bandit.labs.overthewire.org -p 2220
9. cat sshkey.private                                                           (Copy Private Key)
10. exit
11. nano sshkey.private                                                         (Paste Private Key)
12. ls -la
13. ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220          (WARNING UNPROTCTED PRIVATE KEY FILE)
14. chmod 600 sshkey.private
15. ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
16. ls
17. ls -a
18. cat /etc/bandit_pass/bandit14                                                (Password Retreived)
19. exit
```

### Reflection:

This level introduced key based authentication over ssh rather than traditional passwords through the use of an ssh private key to authenticate as another and retrieve the password. A point of interest here was the importance of private key security; here, the assigned key permissions to the private key were a primary determinant for whether the key is treated as valid or not, as the key acts as the digital signature that guarantees the identity of the user, hence preventing accidental leaks by enforcing least privilege permissions becomes fundamental.
