### Level Goal:

The goal of this level was to retrieve the password which was stored in a file called "-" located in the home directory

### Commands Used:

```bash
    1. ssh bandit1@bandit.labs.overthewire.org -p 2220
    2. ls
    3. cat ./-   (Password Retrieved)
    4. exit
```

### Reflection:

This level introduced the fact that files with names that begin with dashes in Linux/Unix based systems are not handled the same way as files without them. Since dashes indicate the passing of a flag/option, attempting to read a file whose filename starts with a dash without proper handling tells the shell that you are attempting to pass a flag which would then be invalid. I learned that proper handling of such filenames means prefixing the file with the relative path of the file (./<dashed-filename>).
