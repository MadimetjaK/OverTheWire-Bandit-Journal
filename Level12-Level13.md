## Level Goal:

The goal of this level was for me to retrieve the password which was stored in the file data.txt, and was a hexdump of a file that has been repeatedly compressed.

### Commands Used:

```bash
1. ssh bandit12@bandit.labs.overthewire.org -p 2220
2. ls
3. man xxd
4. xxd –r data.txt
5. cat data.txt
6. mkdir /tmp/newdatafile
7. cp data.txt /tmp/newdatafile
8. cd /tmp/newdatafile
9. ls
10. xxd -r data.txt > reverseddata
11. file reverseddata                       (reverseddata: gzip compressed data, was "data2.bin", last modified: Wed Jun 24 14:58:46 2026, max compression, from Unix, original size modulo 2^32 580)
12. man gzip
13. gzip -d reverseddata                    (gzip: reverseddata: unknown suffix – ignored)
14. mv reverseddata ndata.gz
15. gzip -d ndata.gz
16. ls
17. file ndata                              (ndata: bzip2 compressed data, block size = 900k)
18. man bzip2
19. mv ndata ndata.bz2
20. bzip2 -d ndata.bz2
21. ls
22. file ndata                              (ndata: POSIX tar archive (GNU))
23. man tar
24. mv ndata ndata.tar
25. tar xf ndata.tar
26. ls
27. file data5.bin                          (data5.bin: POSIX tar archive (GNU))
28. ls
29. mv data5.bin data5.tar
30. tar xf data5.tar
31. ls
32. file data6.bin                          (data6.bin: bzip2 compressed data, block size = 900k)
33. mv data6.bin ndata.bz2
34. bzip2 -d ndata.bz2
35. ls
36. file ndata                              (ndata: POSIX tar archive (GNU))
37. mv ndata ndata.tar
38. ls
39. tar xf ndata.tar
40. ls
41. file data8.bin                          (data8.bin: gzip compressed data, was "data9.bin", last modified: Wed Jun 24 14:58:46 2026, max compression, from Unix, original size modulo 2^32 49)
42. mv data8.bin ndata.gz
43. ls
44. gzip -d ndata.gz
45. ls
46. file ndata                              (ndata: ASCII text)
47. cat ndata                               (Password Retrieved)
48. exit
```

### Reflection:

This level introduced hexdump reversing through the "xxd" utility, manual file decompression through the archiving utilities "tar" and "gzip", and reinforced filetype identification through file headers through the "file" command, which all enabled me to retrieve the password.
