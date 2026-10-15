## Level Goal:

The goal of this level was for me to retrieve the password which was stored in the only human-readable file in the inhere directory.

### Commands Used:

```bash
1. ssh bandit4@bandit.labs.overthewire.org -p 2220
2. ls
3. cd inhere
4. file -file00 (file: Cannot open `ile00'     (No such file or directory))
5. file ./"-file00"                            (./-file00: data)
6. file ./"-file01"                            (./-file01: data)
7. file ./"-file02"                            (./-file02: OpenPGP Secret Key)
8. cat ./"-file02"
9. file ./"-file03"                            (./-file03: data)
10. file ./"-file04"                           (./-file04: data)
11. file ./"-file05"                           (./-file05: Non-ISO extended-ASCII text, with NEL line terminators)
12. file ./"-file06"                           (./-file06: data)
13. file ./"-file07"                           (./-file07: ASCII text)
14. cat ./"-file07"                            (Password Retrieved)
15. exit
```

### Reflection:

This level introduced filetype parsing using the "file" command, which I used to identify the file with the ASCII text to retrieve the password. I learnt that since the Linux filenames can sometimes have no extension at all, filetype parsing with this tool allows me to determine a filetype by its contents.
