# Bandit Level 4 > Level 5

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

> Commands you may need to solve this level
> `ls` , `cd` , `cat` , `file` , `du` , `find`

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

The result of this command shows there are several files named `-file00`, `-file01`, and so on up to `-file09`. However, not all files can be directly read by humans.

To find human-readable files, use the following command to check the file type:

```
file ./*
```

This command will show that most of the files are of data type, except for one file of ASCII text type, namely `-file07`. After knowing that -file07 is a human-readable text file, open the file with the command:

```
more ./-file07
```

![alt text](/OverTheWire/Bandit/images/Bandit4.png)


