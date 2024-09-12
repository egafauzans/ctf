# Bandit Level 5 > Level 6

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
First, check all the contents of the current directory including the hidden files. This can be done with the following command:

```
ls -la
```

we can see there is a hidden directory called *inhere*. Go into that directory and look at the contents.

```
cd inhere/ 
ls -la
```

It shows many subdirectories with the names `maybehere00`, `maybehere01`, and so on up to `maybehere19`.

To find the required file, use the following command to check the file:

```
find ./ -type f -size 1033c ! -executable -readable 2>/dev/null
```

| Option | Description |
| ----------- | ----------- |
| ./ | This starts in the current directory (`./`) and all its subdirectories. |
| -type f | This option limits the search to regular files (not directories or special file types). |
| -size 1033c | This filters files to only include those that are exactly 1033 bytes in size. The c after the size specifies that the unit is bytes. |
| ! -executable | The `!` negates the condition, so this excludes files that are executable (i.e., files that do not have executable permissions). |
| -readable | This ensures that the search includes only files that the current user can read (human-readable). |
| 2>/dev/null | This part redirects error messages (like permission errors) to `/dev/null`, which effectively hides them from the terminal output. |

After that, you will find the corresponding file which is `./maybehere07/.file2`. Kamu menggunakan perintah `more` untuk membuka dan membaca isi file tersebut:

```
more ./maybehere07/.file2
```

![alt text](/OverTheWire/Bandit/images/Bandit5.png)
