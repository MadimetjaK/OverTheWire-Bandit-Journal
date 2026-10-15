### Level Goal:

The goal of this level was for me to retrieve the password which was stored in a file called --spaces in this filename-- located in the home directory.

### Commands Used:

```bash
    ssh bandit2@bandit.labs.overthewire.org -p 2220
    ls
    cat '--spaces in this filename--'        (error: unexpected argument '--spaces in this filename--' found)
    cd "--spaces in this filename--"         (-bash: cd: --: invalid option)
    cat "-- --spaces in this filename--"     (error: unexpected argument '-- --spaces in this filename--' found)
    pwd
    ls –l
    cat ./ "--spaces in this filename--"     (Password Retrieved)
    exit
```

### Reflection:

The level introduced simple directory enumeration through the "ls" command and file reading with the "cat" command. The use of port 2220 for the ssh connection instead of the standard port 22 also taught me that protocols are agnostic of port numbers and services such as ssh can be instructed to bind to any unused port, something I was not aware of.  
