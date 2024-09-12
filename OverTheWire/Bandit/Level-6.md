# Bandit Level 6 > Level 7

The password for the next level is stored somewhere on the server and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
To find the file that meets the specific criteria, you can use the following `find` command:

```
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

| Option | Description |
| ----------- | ----------- |
| / | This tells find to search from the root directory (i.e., search the entire system). |
| -user bandit7 | This filters the search to files owned by the user `bandit7`. |
| -group bandit6 | This filters the search to files that belong to the group `bandit6`. |
| -size 33c | This looks for files that are exactly 33 bytes in size (the `c` indicates bytes). |
| 2>/dev/null | This redirects any error messages (like permission errors) to `/dev/null`, so they won’t clutter your terminal. |

Once you find the file, you can use the cat command to view its content and retrieve the password for the next level:

```
more /var/lib/dpkg/info/bandit7.password
```

![alt text](/OverTheWire/Bandit/images/Bandit6.png)
