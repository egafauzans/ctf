# Bandit Level 12 > Level 13

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

> Commands you may need to solve this level
> `man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

### 1. Remote the instance
Can be done by following the previous method.

### 2. Find the password
We were told earlier that the password is contained in a hex dump file. As we can see from the image, the file is completely unreadable. We were also told that the file was compressed several times. To decompress it, we need a directory with read and write permissions. 

![alt text](/OverTheWire/Bandit/images/Bandit12-1.png)

```
ls -al
mkdir /tmp/ega
cp data.txt /tmp/ega
cd /tmp/ega 
ls -la
more data.txt
```

![alt text](/OverTheWire/Bandit/images/Bandit12-2.png)

After creating the new directory needed, we will copy the file to decompress. Earlier we saw that `data.txt` is not readable at all. There is a `xxd` command to create a hex dump of a file. However, this command also has a reverse function or serves to restore the hexdump into the original file. 

Convert the hex dump file to binary using the `xxd` command with the `-r` option, and save the output as `data1`. Check the file type of `data1` with the file command to see if it is compressed.

```
xxd -r data.txt data1
file data1
mv data1 data2.gz
gzip -d data2.gz
file data2
mv data2 data3.bz2
bzip2 -d data3.bz2
file data3
mv data3 data4.gz
gzip -d data4.gz
file data4
tar -xvf data4
file data5.bin
tar -xvf data5.bin
file data6.bin
mv data6.bin data7.bz2
bzip2 -d data7.bz2
file data7
tar -xvf data7
file data8.bin
mv data8.bin data9.gz
gzip -d data9.gz
file data9
more data9
```

If `data1` is a gzip-compressed file, rename it to `data2.gz` and decompress it with the `gzip -d` command. If the resulting file is still unreadable, check its type again. If it is identified as bzip2 compressed, rename it to `data3.bz2` and decompress it with `bzip2 -d`. Continue this process if it turns out to be gzip-compressed again by renaming it to data4.gz and decompressing it.

If you come across a tar archive, extract its contents using the `tar xvf` command, which may produce additional files. If any of these files are bzip2 compressed, rename them with a `.bz2` extension and decompress them. Follow up with tar extraction if necessary. Continue this process of renaming, decompressing, and extracting until you have a final file that is an ASCII text file.

Once you have the final ASCII text file, use the `cat` or `more` command to read its contents and retrieve the password for the next level.
