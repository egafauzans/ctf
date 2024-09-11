# Bandit Level 2 > Level 3

The password for the next level is stored in a file called spaces in this filename located in the home directory

> Commands you may need to solve this level
> `ls` , `cd` , `cat` , `file` , `du` , `find`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
First, check the contents of the current directory. Can be done with the following command:

```
ls
```

Then we will see a file called *spaces in this filename*. we can see its contents with the `cat` or `more` command.

```
more spaces\ in\ this\ filename 
```

Then we will find the password we are looking for.

![alt text](/OverTheWire/Bandit/images/Bandit2.png)


