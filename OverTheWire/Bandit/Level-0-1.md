# Bandit Level 0 > Level 1

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

> Commands you may need to solve this level
> `ls` , `cd` , `cat` , `file` , `du` , `find`

**TIP**: Create a file for notes and passwords on your local machine!

Passwords for levels are not saved automatically. If you do not save them yourself, you will need to start over from bandit0.

Passwords also occassionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you’ve completed the challenge.

### 1. Remote the instance
Can be done by following the level 0 method, but I use a third-party ssh client to make things easier.

### 2. Find the password
First, check the contents of the current directory. Can be done with the following command:

```
ls
```

Then we will see a file called *readme*. we can see its contents with the `cat` or `more` command.

```
more readme
```

Then we will find the password we are looking for.

![alt text](/OverTheWire/Bandit/images/Bandit0-3.png)