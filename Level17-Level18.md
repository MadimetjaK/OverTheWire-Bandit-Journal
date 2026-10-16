## Level Goal:

The goal of this level was for me to retrieve the password which was in passwords.new and was the only line that has been changed between the old passwords file (passwords.old) and the new passwords file (passwords.new) in the home directory.

### Commands Used:

```bash
1. ssh bandit17@bandit.labs.overthewire.org -p 2220
2. ls
3. cat passwords.new
4. man diff
5. diff passswords.new passwords.old       (Password Retrieved)
6. exit
```

### Reflection:

This level introduced file comparison through the file comparison utility "diff" tool, which enabled me to retrieve the password by finding and displaying the exact line by line difference between two password files.
