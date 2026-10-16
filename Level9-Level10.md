## Level Goal:

The goal of this level was for me to retrieve the password which was stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters

### Commands Used:

```bash
1. ssh bandit9@bandit.labs.overthewire.org -p 2220
2. ls
3. grep “-” data.txt           (grep: data.txt: binary file matches)
4. man strings
5. strings data.txt            (Password Retrieved)
6. exit
```

### Reflection:

This level also reinforced text search and filtering through the binary analysis utility "strings", which enabled me to look for any sequence of human readable printable characters in the data.txt file to retrieve the password. The point of interest for me here was the difference betweeen the strings command and the grep command. Here I learnt that their difference lies in the filetype they target respectively, where grep primarily is for targeting human readable text files such as configuration files and strings is for targeting non human readable files such as memory dumps.
