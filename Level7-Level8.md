### Level Goal:

The goal of this level was for me to retrieve the password which was stored in the file data.txt next to the word millionth.

### Commands Used:

```bash
1. ssh bandit7@bandit.labs.overthewire.org -p 2220
2. ls
3. man grep
4. grep “millionth” data.txt
5. exit
```

### Reflection:

The level introduced me to text search and filtering through the "grep" command, which is a utility that enables me to find and read text within a file by retrieving the line in the file where the specified text sits. Since this is a line-oriented utility, knowing any value within the sought after line in a file allows you to retrieve every other value that shares line space with it.
