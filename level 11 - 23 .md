# Over The Wire

## Challenge: Bandit Level 10 → Level 11

Encoding is not encryption and offers no real security.

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

Encoding is not encryption and offers no real security.

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

Encoding is not encryption and offers no real security.

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

Encoding is not encryption and offers no real security.

**Commands Used:**
```bash
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' N-ZA-Mn-za-m
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
**passord for next level:**
```bash
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
