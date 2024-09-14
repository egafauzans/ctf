# Bandit Level 8 > Level 9

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

> Commands you may need to solve this level
> `man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We can start by checking the contents of our current directory

```
ls -al
```

![alt text](/OverTheWire/Bandit/images/Bandit8-1.png)

We can look at and examine a file called data.txt. As you can see, the data.txt file contains a lot of information. 

```
more data.txt
```

To display the unique lines from `data.txt` that appear only once, we first sort the file and then use uniq -u to remove any repeated lines, showing only the unique ones.

```
sort data.txt | uniq -u
```

| Option | Description |
| ----------- | ----------- |
| sort data.txt | This sorts the lines in `data.txt` in alphabetical or lexicographical order. |
| pipe operator | The pipe takes the output of one command (in this case, `sort data.txt`) and sends it as input to the next command (`uniq`). |
| uniq -u | `uniq` removes adjacent duplicate lines but with the -u option, it will only print lines that are unique (i.e., lines that appear only once in the file). |

![alt text](/OverTheWire/Bandit/images/Bandit8-2.png)

The result of running the sort and uniq combination shows the unique line (the password).