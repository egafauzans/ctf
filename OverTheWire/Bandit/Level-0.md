# Bandit Level 0

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is *bandit.labs.overthewire.org*, on port *2220*. The username is *bandit0* and the password is *bandit0*. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### 1. Open Terminal
Open your terminal (command prompt or powershell if you using windows operating system).

### 2. Remote the instance
Remote the instance using ssh. The format for ssh is 

`ssh username@hostname -p port -i keypair`

From the challenge we know that:

| Parameter | Value |
| ----------- | ----------- |
| username | bandit0 |
| hostname | bandit.labs.overthewire.org |
| port | 2220 |
| password | bandit0 |

so that we can change the command to:

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

then answer *yes* to *Are you sure you want to continue connecting (yes/no/[fingerprint])? * then enter the password. The passwords are hidden in terminal!

![alt text](/OverTheWire/Bandit/images/Bandit0-1.png)
![alt text](/OverTheWire/Bandit/images/Bandit0-2.png)

