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

This level reinforced text search and filtering through the text reordering utility "sort" and the duplicate line filtering utility "uniq", which both enabled me to reorder the data.txt file and filter for any unique value in order to retrieve the password. Another point of interest was the pipe utility "|" which is a utility that enabled me to pass the reordered results from the "sort" command directly to the "uniq" command to retrieve the passsword. This utility allows me to chain multiple single purpose utilities together to make a more robust command.
