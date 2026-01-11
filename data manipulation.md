# Linux Luminarium

## Module 8: Data manipulation

### Challenge: Translating charecters

**Commands Used:**
```bash
hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'
```
**Output:**
```bash
yOUR CASE-SWAPPED FLAG:
pwn.college{IjtmvZYMyVZOl_-EjyTLjyHjOfa.01MxEzNxwCM3UzNzEzW}
```

### Challenge: Deleting charecters

**Commands Used:**
```bash
hacker@data~deleting-characters:~$ /challenge/run |tr -d ^%
```
**Output:**
```bash
Your character-stuffed flag:
pwn.college{Eb5II0tUNYtIYXoC7N3m4Z6ixlO.0FNxEzNxwCM3UzNzEzW}
```

### Challenge: Deleting newlines

**Commands Used:**
```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
```
**Output:**
```bash
Your line-split flag: pwn.college{MB_Gvee9o1LeSwH9MKOewTNSBsj.0VNxEzNxwCM3UzNzEzW}
```

### Challenge: Extrating the first line with head

**Commands Used:**
```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college 
```
**Output:**
```bash
Congratulations, you piped the right codes!
pwn.college{8JNzUlOx-U98qX4KxRQ9KkOKVbP.0lNxEzNxwCM3UzNzEzW}
```

### Challenge: Extracting specific sections of text

**Commands Used:**
```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run 
19871 p
9873 w
7617 n
28515 .
26399 c
21505 o
17415 l
23125 l
8683 e
31009 g
7674 e
13976 {
17224 I
21849 O
22019 d
7974 t
2296 g
1099 u
6396 z
21684 B
3819 F
964 C
20969 8
17526 P
23417 h
171 -
1137 1
21398 g
10884 G
43 y
15847 4
4993 L
7746 0
15562 g
10418 q
19902 c
29969 f
19503 E
24660 e
18203 .
30104 0
29881 1
24222 N
28273 x
24429 E
9978 z
31589 N
12204 x
20700 w
19020 C
31453 M
23212 3
28394 U
24686 z
25609 N
18777 z
460 E
11686 z
6565 W
14525 }
data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
```
**Output:**
```bash
pwn.college{IOdtguzBFC8Ph-1gGy4L0gqcfEe.01NxEzNxwCM3UzNzEzW}
```

### Challenge: Sorting data

**Commands Used:**
```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt -r
```
**Output:**
```bash
pwn.college{Unn9vJJaysatn-9KByohdtsf4ep.0FM0MDOxwCM3UzNzEzW}
```
