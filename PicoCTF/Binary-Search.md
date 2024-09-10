# Binary Search

Using a Secure Shell (SSH) is going to be pretty important.

Can you ssh as *ctf-player* to *titan.picoctf.net* at port *64606* to get the flag?

You'll also need the password *83dcefb7*. If asked, accept the fingerprint with *yes*.

![alt text](/PicoCTF/images/BinarySearch.png)

### 1. Open Terminal
Open your terminal (command prompt or powershell if you using windows operating system).

### 2. Remote the instance
Remote the instance using ssh. The format for ssh is 

`ssh username@hostname -p port -i keypair`

From the challenge we know that:

| Parameter | Value |
| ----------- | ----------- |
| username | ctf-player |
| hostname | titan.picoctf.net |
| port | 64606 |
| password | 83dcefb7 |

so that we can change the command to:

```
ssh ctf-player@titan.picoctf.net -p 64606
```

then answer *yes* to *Are you sure you want to continue connecting (yes/no/[fingerprint])? * then enter the password. The password will not be visible when we enter it. 

### 3. Grab the flag
After successfully remoting the instance, the flag will be visible. We just need to copy the flag and paste it into the challenge.