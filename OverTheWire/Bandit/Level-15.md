# Bandit Level 15 > Level 16

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

> Commands you may need to solve this level
> `ssh`, `telnet`, `nc`, `ncat`, `socat`, `openssl`, `s_client`, `nmap`, `netstat`, `ss`

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We are told that the password for the next level can be obtained by sending the password for the current level to port 30000 on localhost. 

![alt text](/OverTheWire/Bandit/images/Bandit15-1.png)
![alt text](/OverTheWire/Bandit/images/Bandit15-2.png)
