# over-the-wire-bandit

## Level 0

Command - ```ssh bandit0@bandit.labs.overthewire.org -p 2220```

Explanation - The port was changed using **-p** option.

## Level 0 -> Level 1

Commands -
```
1. cat readme
2. Ctrl+D (To disconnect from server)
```

## Level 1 -> Level 2

Command - ```cat < -```

Explanation - The shell considers **"-"** to be an option, therefore we use the redirection operator.

## Level 2 -> Level 3

Command - ```cat "spaces in this filename"```

Explanation - We need to use quotes otherwise it will search for files with names "spaces", "in", "this" and "filename" individually.

## Level 3 -> Level 4

Commands -
```
1. cd inhere
2. ls -a
3. cat .hidden
```

Explanation - The **-a** option shows both visible and hidden files present in a directory.

## Level 4 -> Level 5

Commands -
```
1. cd inhere
2. file -- *
3. cat -- -file07
```

Explanation - The names of all files start with a **"-"** so we use **"--"** to ignore further options and the **"*"** is used to check all files.

## Level 5 -> Level 6

Commands -
```
1. cd inhere
2. find -readable ! -executable -size 1033c
```

Explanation - **"c"** specifies byte.

## Level 6 -> Level 7

Commands -
```
1. cd /
2. find 2>/dev/null -user bandit7 -group bandit6 -size 33c
```

Explanation - Went to the root folder then searched according to the given conditions. **2>/dev/null** avoids all displays where the Permission was denied.

## Level 7 -> Level 8

Command - ```grep "millionth" data.txt```

## Level 8 -> Level 9

Command - ```sort data.txt | uniq -u```

Explanation - **Uniq** command removes duplicate strings only if they are adjacent. Used the **-u** tag to print the string that occurs only once.

## Level 9 -> Level 10

Command - ```grep -a "=====" data.txt```

Explanation - The **"-a"** tag processes a binary file as if it were text. Manually searched for something that looked like a readable string🤷‍♀️.

## Level 10 -> Level 11

Command - ```base64 -d data.txt```

Explanation - The **"-d"** tag decodes the data.

## Level 11 -> Level 12

Command - ```cat data.txt | tr '[a-z]' '[n-za-m]' | tr '[A-Z]' '[N-ZA-M]'```

Explanation - Rotated the small characters first and then the second characters. **NOTE:** Rotation by 13 is an inverse of itself.

## Level 12 -> Level 13

Commands -
```
1. cd /tmp
2. mktemp -d (Created a directory tmp.of7TAHaLRc)
3. cd /tmp/tmp.of7TAHaLRc
4. cp /home/bandit12/data.txt aisehi.txt
5. xxd -r aisehi.txt > 1.txt
6. file 1.txt (gzip compressed data)
7. mv 1.txt 1.gz
8. gunzip 1.gz
9. ls
10. cat 1
11. file 1 (bzip2 compressed data)
12. mv 1 1.bz2
13. bunzip2 1.bz2
14. ls
15. file 1 (gzip compressed data)
16. mv 1 1.gz
17. gunzip 1.gz
18. ls
19. file 1 (POSIX tar archive (GNU) )
20. man tar
21. mv 1 1.tar
22. tar -xf 1.tar
23. ls
24. file data5.bin (POSIX tar archive (GNU) )
25. tar -xf data5.bin
26. ls
27. file data6.bin (bzip2 compressed data)
28. bunzip2 data6.bin
29. ls
30. file data6.bin.out (POSIX tar archive (GNU) )
31. tar -xf data6.bin.out
32. ls
33. file data8.bin (gzip compressed data)
34. mv data8.bin 2.gz
35. gunzip 2.gz
36. ls
37. file 2 (ASCII text)
38. cat 2
```

Explanation - The extensions of gzip, bzip2 and tar archives are **.gz, .bz2 and .tar** respectively. To unzip a compressed file we need to rename the file name to have the appropriate extension.

## Level 13 -> Level 14

Command - ```ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220```

Explanation - Connected to a remote server using private key. **-i** option is used to select a file from which the key has to be read.

## Level 14 -> Level 15
