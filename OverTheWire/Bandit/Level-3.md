# Bandit Level 3 > Level 4

The password for the next level is stored in a hidden file in the inhere directory.

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

We can see the contents of the *...Hiding-From-You* file and we will find the password we are looking for.

Then we will find the password we are looking for.

![alt text](/OverTheWire/Bandit/images/Bandit3.png)


