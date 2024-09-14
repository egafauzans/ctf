# Bandit Level 11 > Level 12

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

> Commands you may need to solve this level
> `man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We can start by checking the contents of our current directory

```
ls -al
```

![alt text](/OverTheWire/Bandit/images/Bandit11.png)

```
more data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
```

### What is ROT13?

ROT13 (rotate by 13 places) is a simple substitution cipher used in cryptography. It operates by shifting each letter in the alphabet by 13 positions. This means:

- A becomes N
- B becomes O
- C becomes P
- ... and so on, up to:
- M becomes Z

Similarly, the process is reversible, so if you apply ROT13 to a letter that’s already been shifted, it will revert to the original letter.

[Helpful Reading](https://en.wikipedia.org/wiki/ROT13)

### What is the `tr` Command?

The `tr` command is a utility in Unix-like operating systems used for translating or deleting characters. It's often used in conjunction with pipes (`|`) to process text.

The basic syntax for tr is:
```
tr [SET1] [SET2]
```

Here, SET1 represents the characters to be replaced, and SET2 represents the characters that will replace them.

[Source by ChatGPT](https://chatgpt.com/)