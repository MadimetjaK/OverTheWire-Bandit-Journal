### Level Goal:

The goal of this level was for me to retrieve the password which was stored in a file called --spaces in this filename-- located in the home directory.

### Commands Used:

```bash
    1. ssh bandit2@bandit.labs.overthewire.org -p 2220
    2. ls
    3. cat '--spaces in this filename--'        (error: unexpected argument '--spaces in this filename--' found)
    4. cd "--spaces in this filename--"         (-bash: cd: --: invalid option)
    5. cat "-- --spaces in this filename--"     (error: unexpected argument '-- --spaces in this filename--' found)
    6. pwd
    7. ls –l
    8. cat ./ "--spaces in this filename--"     (Password Retrieved)
    9. exit
```

### Reflection:

This level introduced taught me that files that have spaces in the filename in Linux/Unix based systems are interpreted as separate commands if not handled properly. Proper handling of files that have spaces in the filename include enclosing the filename in quotations to instruct the shell to read it as one string.
