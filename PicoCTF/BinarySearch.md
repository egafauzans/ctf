# Binary Search

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

`ssh -p 55441 ctf-player@atlas.picoctf.net`
Using the password *6dd28e9b*. Accept the fingerprint with *yes*, and *ls* once connected to begin. Remember, in a shell, passwords are hidden!

![alt text](/PicoCTF/images/SuperSSH.png)

### 1. Open Terminal
Open your terminal (command prompt or powershell if you using windows operating system).

### 2. Remote the instance
Remote the instance using the ssh command and type the password:

```
ssh -p 55441 ctf-player@atlas.picoctf.net
```

### 3. Find the flag
After successfully remoting the instance, a message will appear as below instructing us to guess a number between 1 - 1000.

```
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess:
```

This message tells us the next clue after we guess a number. It will tell us 'Lower!' or 'Higher!' of the number we have entered. 

We are asked to keep guessing until we find the number we are looking for. However, there is a limit of 10 guesses, after which the instance will shut down. 

To overcome this, we must guess the numbers efficiently. We will use the binary search method to guess the number by continuing to divide the two numbers until we find the right number. 

Then when the number we guess is correct, the flag will appear.

![alt text](/PicoCTF/images/BinarySearch.png)