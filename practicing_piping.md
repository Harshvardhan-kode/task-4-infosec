# Linux Luminarium

## Module 6: Practicing Piping

### Challenge: redirecting output

**Commands Used:**
```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
```
**Output:**
```bash
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{Ea353ceVyQyVjsYueJncq7KqAtZ.QX0YTN0wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: redirecting more output

**Commands Used:**
```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag
```
**Output:**
```bash

[FLAG] Here is your flag:
[FLAG] pwn.college{k9-7XQLM4tbnhYy-xF7meIyDDfb.QX1YTN0wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: appending output

**Commands Used:**
```bash
hacker@piping~appending-output:~$ rm -f /home/hacker/the-flag
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
```
**Output:**
```bash
 | 
\|/ This is the first half:
 v 
pwn.college{QQLAxN-1JWsO4amtEx0KoqTB46m.QX3ATO0wCM3UzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```

## Module 6: Practicing Piping

### Challenge: redirecting errors

**Commands Used:**
```bash
hacker@piping~redirecting-errors:~$ /challenge/run
hacker@piping~redirecting-errors:~$ /challenge/run >myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions 
```
**Output:**
```bash

[FLAG] Here is your flag:
[FLAG] pwn.college{8rNW1M5bNkxkDJKjBDy-i0iFwCp.QX3YTN0wCM3UzNzEzW}

```

## Module 6: Practicing Piping

### Challenge: redirecting input

**Commands Used:**
```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ /challenge/run < PWN
``` 
**Output:**
```bash
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{Yzh4DfnM0-sG3NAIwoSv5Mo5456.QXwcTN0wCM3UzNzEzW}

```

## Module 6: Practicing Piping

### Challenge: grepping stored results

**Commands Used:**
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
pwn.college{MXDrZDxHXxZAOJtmCFMngtM5Po0.QX4EDO0wCM3UzNzEzW}
```
**Output:**
```bash
pwning
pwn
pwn.college{MXDrZDxHXxZAOJtmCFMngtM5Po0.QX4EDO0wCM3UzNzEzW}
pwns
pwned
```

## Module 6: Practicing Piping

### Challenge: grepping live output

**Commands Used:**
```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep "{"
```
**Output:**
```bash
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{4xWdznDPLlL2EfDUriPhb1G63Gm.QX5EDO0wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: grepping errors

**Commands Used:**
```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep "{"
```
**Output:**
```bash
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{YQNY8D5WM9qAlLQDKZpxJlEVbyd.QX1ATO0wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: filtering with grep -v 

**Commands Used:**
```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
```
**Output:**
```bash
pwn.college{QXsGacfoi6pI5LBe3hUtHpLKNSI.0FOxEzNxwCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: filtering with sed

**Commands Used:**
```bash
hacker@piping~filtering-with-sed:~$ /challenge/run | sed "s/FAKEFLAG/ /g"
p w n . c o l l e g e { g C p 3 V - J R 2 I N s e U W 4 c u I x 0 j D N 0 V k . 0 1 N x Q T M y w C M 3 U z N z E z W }
hacker@piping~filtering-with-sed:~$ /challenge/run | sed "s/FAKEFLAG//g"
```
**Output:**
```bash
pwn.college{gCp3V-JR2INseUW4cuIx0jDN0Vk.01NxQTMywCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: Duplicating piped data with tee

**Commands Used:**
```bash
hacker@piping~duplicating-piped-data-with-tee:~$ cat /tmp/intercept 
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "UWrueH5E"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret UWrueH5E | tee /tmp/intercept | /challenge/college 
```
**Output:**
```bash
Processing...
WARNING: you are overwriting file /tmp/intercept with tee's output...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{UWrueH5EdkRlNJ6rsIeXYiI3LhC.QXxITO0wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: process substitution for input

**Commands Used:**
```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys_and_flag) <(/challenge/print_decoys)
13d12
```
**Output:**
```bash
pwn.college{4qDIrOzstChlCWK7iMWJjJXs6CK.0lNwMDOxwCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: writing to multiple programs

**Commands Used:**
```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
```
**Output:**
```bash
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
27457119182978626446
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{MTNJJoCkTDYpuSq88nRv1qVngpc.QXwgDN1wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: split-piping stderr and stdout

**Commands Used:**
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
```
**Output:**
```bash
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{oAUhuA1V34BIZZ2xx-nJG19Q4JG.QXxQDM2wCM3UzNzEzW}
```

## Module 6: Practicing Piping

### Challenge: named pipes

**Commands Used:**
```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of /challenge/run.
Recall that operations on FIFOs will *block* until both the read side and the write side is open,
so /challenge/run will not actually be aunched until you start reading from the FIFO!
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
```
**Output:**
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at /tmp/flag_fifo!
Here is your flag: 
pwn.college{QyBSElEX4Rbx29X9y3cGEmqUwLC.01MzMDOxwCM3UzNzEzW}
```
