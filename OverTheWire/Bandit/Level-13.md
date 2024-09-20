# Bandit Level 13 > Level 14

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

> Commands you may need to solve this level
> `ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We were told that we would not be given a password for the next level. Instead, we will be given a private key. So to get to the next level, we will use this private key. First, let's use the ls command to find the private key. We found the private key. Now we will use it to get an SSH connection as bandit14.
![alt text](/OverTheWire/Bandit/images/Bandit13-2.png)

```
ls -la
ssh bandit14@bandit.labs.overthewire.org -p 2220 -i sshkey.private
```

If we look at the contents of the private key, it contains information that serves to decrypt messages or data that has been encrypted by the public key. We can copy it and store it on our personal computer to access level 14 in the future. 

![alt text](/OverTheWire/Bandit/images/Bandit13-1.png)