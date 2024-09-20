# Bandit Level 14 > Level 15

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

> Commands you may need to solve this level
> `ssh`, `telnet`, `nc`, `openssl`, `s_client`, `nmap`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We are told that the password for the next level can be obtained by sending the password for the current level to port 30000 on localhost. 

First, I used nmap to scan for open TCP ports on localhost, which revealed several services running, including one on port 30000. Next, I tried using netcat to connect to localhost on port 3000, but that failed. I then used netcat to connect to port 30000, which prompted me for a password. I then looked up the password for `bandit14` in `/etc/bandit_pass/bandit14` using `more` command, which revealed the correct password. Finally, I successfully entered this password into netcat on port 30000, which confirmed it was correct and revealed the next password.

![alt text](/OverTheWire/Bandit/images/Bandit14.png)

```
more /etc/bandit_pass/bandit14
nc localhost 30000
```

| Option | Description |
| ----------- | ----------- |
| nmap | Nmap (Network Mapper) is an open-source tool used for network discovery and security auditing. |
| -s | This prefix is common in `nmap` options to specify a scan type. |
| T | Refers to a TCP connect scan. |

Theres other scan option that nmap offers:

| Option | Description |
| ----------- | ----------- |
| -sS | (SYN Scan) Also known as stealth scan, this is often faster and less detectable than a TCP connect scan. |
| -sU | (UDP Scan) To scan for open UDP ports. |
| -sV | (Service Version Detection) To detect versions of the services running on open ports. |
| -O | (OS Detection) To determine the operating system of the target. |
| -sI | (Idle Scan) A more stealthy scanning technique that uses a third-party host to send packets. |
| -sA | (TCP ACK Scan) Used to map out firewall rulesets. |

Netcat, often referred to as "nc", is a versatile networking utility for reading from and writing to network connections using TCP or UDP. It's sometimes called the "Swiss Army Knife" of networking due to its wide range of capabilities.



