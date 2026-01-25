# Over The Wire

## Challenge: Bandit Level 10 → Level 11

**Commands Used:**
```bash
bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
**passord for next level:**
```bash
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

## Challenge: Bandit Level 11 → Level 12

**Commands Used:**
```bash
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' N-ZA-Mn-za-m
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
**passord for next level:**
```bash
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

## Challenge: Bandit Level 12 → Level 13

**Commands Used:**
```bash
bandit12@bandit:~$ cd /tmp
bandit12@bandit:/tmp$ mktemp -d
/tmp/tmp.dRKrORdaKR
bandit12@bandit:/tmp$ cd /tmp/tmp.dRKrORdaKR
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ cp ~/data.txt .
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ ls
data.txt
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ xxd -r data.txt data
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: gzip compressed data, was "data2.bin", last modified: Tue Oct 14 09:26:00 2025, max compression, from Unix, original size modulo 2^32 572
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data2.bin data
mv: cannot stat 'data2.bin': No such file or directory
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.gz
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ gunzip data.gz
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.bz2
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ bunzip2 data.bz2
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: gzip compressed data, was "data4.bin", last modified: Tue Oct 14 09:26:00 2025, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.gz
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ gunzip data.gz
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.tar
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ tar -xf data.tar
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ ls
data5.bin  data.tar  data.txt
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ cat data
cat: data: No such file or directory
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data5.bin data
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.tar
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ tar -xf data.tar
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ ls
data6.bin  data.tar  data.txt
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data6.bin data
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.bz2
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ bunzip2 data.bz2
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.tar
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ tar -xf data.tar
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ ls
data8.bin  data.tar  data.txt
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data8.bin data
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: gzip compressed data, was "data9.bin", last modified: Tue Oct 14 09:26:00 2025, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ mv data data.gz
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ gunzip data.gz
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ file data
data: ASCII text
bandit12@bandit:/tmp/tmp.dRKrORdaKR$ cat data
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
**passord for next level:**
```bash
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

## Challenge: Bandit Level 13 → Level 14

**Commands Used:**
```bash
PS C:\Users\Harshvardhan> scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private .
backend: gibson-0
bandit13@bandit.labs.overthewire.org's password:
sshkey.private                                                                        100% 1679     4.4KB/s   00:00
PS C:\Users\Harshvardhan> ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

```
**passord for next level:**
```bash
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```

## Challenge: Bandit Level 14 → Level 15

**Commands Used:**
```bash
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:~$ nc localhost 30000

Wrong! Please enter the correct current password.
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
**passord for next level:**
```bash
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```

## Challenge: Bandit Level 15 → Level 16

**Commands Used:**
```bash
openssl s_client -connect localhost:30001
..........
read R BLOCK
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

closed
```
**passord for next level:**
```bash
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```

## Challenge: Bandit Level 16 → Level 17

**Commands Used:**
```bash
bandit16@bandit:~$ openssl s_client -connect localhost:31790 -quiet
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
bandit16@bandit:/tmp/gum$ exit
PS C:\Users\Harshvardhan> notepad C:\Users\Harshvardhan\bandit16_rsa
PS C:\Users\Harshvardhan> dir C:\Users\Harshvardhan\Documents

    Directory: C:\Users\Harshvardhan\Documents

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          30-12-2025    23:24                Custom
                                                  Office
                                                  Templates
-a---          25-01-2026    09:39           1700 bandit16_rsa.
                                                  txt

```
**passord for next level:**
```bash
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
```

## Challenge: Bandit Level 17 → Level 18

**Commands Used:**
```bash
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< pGozC8kOHLkBMOaL0ICPvLV1IjQ5F1VA
---
> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```
**passord for next level:**
```bash
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```

## Challenge: Bandit Level 18 → Level 19

**Commands Used:**
```bash
PS C:\Users\Harshvardhan> ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

backend: gibson-1
bandit18@bandit.labs.overthewire.org's password:
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```
**passord for next level:**
```bash
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```

## Challenge: Bandit Level 19 → Level 20

**Commands Used:**
```bash
bandit19@bandit:~$ ls -l
total 16
-rwsr-x--- 1 bandit20 bandit19 14884 Oct 14 09:26 bandit20-do
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do whoami
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```
**passord for next level:**
```bash
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```

## Challenge: Bandit Level 20 → Level 21

**Commands Used:**
```bash
bandit20@bandit:~$ ls -l
total 16
-rwsr-x--- 1 bandit21 bandit20 15608 Oct 14 09:26 suconnect
bandit20@bandit:~$ ./suconnect 4444
Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
Password matches, sending next password

# made a dummy server to interact with the bandit21 with two terminals open one to connect to 21 and the other to verify the password of the level

bandit20@bandit:~$ nc -l 4444
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```
**passord for next level:**
```bash
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```

## Challenge: Bandit Level 21 → Level 22

**Commands Used:**
```bash
bandit21@bandit:~$ ls -l /etc/cron.d/
total 40
-r--r----- 1 root root  47 Oct 14 09:26 behemoth4_cleanup
-rw-r--r-- 1 root root 123 Oct 14 09:19 clean_tmp
-rw-r--r-- 1 root root 120 Oct 14 09:26 cronjob_bandit22
-rw-r--r-- 1 root root 122 Oct 14 09:26 cronjob_bandit23
-rw-r--r-- 1 root root 120 Oct 14 09:26 cronjob_bandit24
-rw-r--r-- 1 root root 201 Apr  8  2024 e2scrub_all
-r--r----- 1 root root  48 Oct 14 09:27 leviathan5_cleanup
-rw------- 1 root root 138 Oct 14 09:28 manpage3_resetpw_job
-rwx------ 1 root root  52 Oct 14 09:29 otw-tmp-dir
-rw-r--r-- 1 root root 396 Jan  9  2024 sysstat
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
```
**passord for next level:**
```bash
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
```

## Challenge: Bandit Level 22 → Level 23

**Commands Used:**
```bash
bandit22@bandit:/etc/cron.d$ ls -l
total 40
-r--r----- 1 root root  47 Oct 14 09:26 behemoth4_cleanup
-rw-r--r-- 1 root root 123 Oct 14 09:19 clean_tmp
-rw-r--r-- 1 root root 120 Oct 14 09:26 cronjob_bandit22
-rw-r--r-- 1 root root 122 Oct 14 09:26 cronjob_bandit23
-rw-r--r-- 1 root root 120 Oct 14 09:26 cronjob_bandit24
-rw-r--r-- 1 root root 201 Apr  8  2024 e2scrub_all
-r--r----- 1 root root  48 Oct 14 09:27 leviathan5_cleanup
-rw------- 1 root root 138 Oct 14 09:28 manpage3_resetpw_job
-rwx------ 1 root root  52 Oct 14 09:29 otw-tmp-dir
-rw-r--r-- 1 root root 396 Jan  9  2024 sysstat
bandit22@bandit:/etc/cron.d$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
andit22@bandit:~$ echo "I am user bandit23" | md5sum
8ca319486bfbbc3663ea0fbe81326349  -
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
```
**passord for next level:**
```bash
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
```
