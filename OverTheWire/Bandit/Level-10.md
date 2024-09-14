# Bandit Level 10 > Level 11

The password for the next level is stored in the file data.txt, which contains base64 encoded data

> Commands you may need to solve this level
> `man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We can start by checking the contents of our current directory

```
ls -al
```

![alt text](/OverTheWire/Bandit/images/Bandit10.png)

The `strings` command extracts and prints all the human-readable text from `data.txt`. This is useful when a file contains both readable and non-readable characters (such as binary data), and we only want to see the text.

The command base64 -d is used to decode a Base64-encoded string back into its original binary or text form.

```
strings data.txt | base64 -d
```

The password is `dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`.