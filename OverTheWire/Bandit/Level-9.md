# Bandit Level 9 > Level 10

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

> Commands you may need to solve this level
> `man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We can start by checking the contents of our current directory

```
ls -al
```

![alt text](image.png)

The `strings` command extracts and prints all the human-readable text from `data.txt`. This is useful when a file contains both readable and non-readable characters (such as binary data), and we only want to see the text.

The `grep` command searches for lines that contain the `=` character from the output of the strings command. It will display only those lines that have one or more `=` characters.

```
strings data.txt | grep =
```

Then we know the password is `FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`.