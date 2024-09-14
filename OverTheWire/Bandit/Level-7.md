# Bandit Level 7 > Level 8

The password for the next level is stored in the file data.txt next to the word millionth.

> Commands you may need to solve this level
> `man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We can start by checking the contents of our current directory

```
ls -al
```

![alt text](/OverTheWire/Bandit/images/Bandit7-1.png)

We can look at and examine a file called data.txt. As you can see, the data.txt file contains a lot of information. 

```
more data.txt
```

The hint says that the flag is stored in the data.txt file next to the word 'millionth'. 

You can use the `grep` command to look for specific keywords or patterns in the file. You can also using pipeline symbol (`|`). The pipe symbol (`|`) takes the output of the `more` command (the content of the file) and sends it to the grep command, which then filters the lines containing 'millionth'.

![alt text](/OverTheWire/Bandit/images/Bandit7-2.png)

As you can see, the command quickly identifies the line with the keyword 'millionth', followed by a string of characters, which is likely the password we're looking for.