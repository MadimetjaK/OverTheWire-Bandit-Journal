## Level Goal:

The goal of this level was for me to retrieve the password which was stored in the file data.txt and was the only line of text that occurs only once.

### Commands Used:

```bash
1. ssh bandit8@bandit.labs.overthewire.org -p 2220
2. man grep
3. grep data.txt | uniq           (uniq: Could not open sort: No such file or directory)
4. cat data.txt
5. man sort
6. sort data.txt uniq –u          (sort: cannot read: uniq: No such file or directory)
7. sort data.txt | uniq –u        (Password Retrieved)
8. exit
```

### Reflection:

This level reinforced me that Linux hides certain files by naming convention. These files have filenames that start with a period {.filename}, and are usually files that store important information such as system configurations.
