# WebDecode

Do you know how to use the web inspector?
Start searching *here* to find the flag

Use the web inspector on other files included by the web page. The flag may or may not be encoded.

### 1. Open the webste for the challenge
Click the hyperlink text 'here' in the challenge.

![alt text](/PicoCTF/images/WebDecode1.png)

### 2. Navigate the page
The hint tells to use web inspector to find the flag. So we can right click on the mouse then select inspect. Or we can also see the entire source code of the page by ctrl + u (I use microsoft edge as a browser, different browsers may have different shortcuts). 

![alt text](/PicoCTF/images/WebDecode2.png)

There doesn't seem to be anything suspicious on this page. However, there is a 'Keep Navigating' clue. Maybe we should keep trying around the navigation buttons, so we will try to enter the *About* menu and then try to do the previous method, which is view the source code. 

![alt text](/PicoCTF/images/WebDecode3.png)

After looking at the source code of the page. There is something suspicious on line 44. Referring to the second clue in the challenge, *The flag may or may not be encoded*, this might be the flag but it is still encoded. So we will try to decode the code. And bingo! The code contains the flag we are looking for. 

![alt text](/PicoCTF/images/WebDecode4.png)