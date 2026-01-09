# Linux Luminarium

## Module 7: Shell variables

### Challenge: Printing variables

**Commands Used:**
```bash
hacker@variables~printing-variables:~$ echo $FLAG
```
**Output:**
```bash
pwn.college{k6DkAMphmjWupgJm0O8yZvoARYC.QX3UTN0wCM3UzNzEzW}
```

### Challenge: Setting variables

**Commands Used:**
```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
```
**Output:**
```bash
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IgFXFkE5y2bWdAFWdxt4h_7EtxH.QX5UTN0wCM3UzNzEzW}
```

### Challenge: Multi-word variables

**Commands Used:**
```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
```
**Output:**
```bash
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{0Y9e4AThWfD5JC1ntKuL_5k0isd.QXwYTN0wCM3UzNzEzW}
```

### Challenge: Exporting variables

**Commands Used:**
```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
```
**Output:**
```bash
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{kx_lYTt1SMQXWAf99fqwiGcdVl0.QXyYTN0wCM3UzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

### Challenge: Printing Exporting variables

**Commands Used:**
```bash
hacker@variables~printing-exported-variables:~$ env
```
**Output:**
```bash
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=e53d7e7324ae1e9a4a217489c88f72deabf8afcbb28e2d782587607419bde3f6
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{Yp9a-ZnF6G5391xufjlVIKjJXAV.QX4UTN0wCM3UzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

### Challenge: Storing command output

**Commands Used:**
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run /flag)

hacker@variables~storing-command-output:~$ echo "$PWN"
```
**Output:**
```bash
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
pwn.college{gzCWOohCHQ1cWxDwLvdxrHd41zT.QX1cDN1wCM3UzNzEzW}
```

### Challenge: Reading input

**Commands Used:**
```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
```
**Output:**
```bash
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{cU4dMVYsD6_fCYB1DLv1yzXal8T.QX4cTN0wCM3UzNzEzW}
```

### Challenge: Reading files

**Commands Used:**
```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me 

```
**Output:**
```bash
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{ku1A7ZE4bLSEi8H6BVcZLXrhamD.QXwIDO0wCM3UzNzEzW}
```
