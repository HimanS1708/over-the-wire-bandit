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

Command- ```cat < -```

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

Command -```sort data.txt | uniq -u```

Explanation - **Uniq** command removes duplicate strings only if they are adjacent. Used the **-u** tag to print the string that occurs only once.

## Level 9 -> Level 10

Command -```grep -a "=====" data.txt```

Explanation - The **"-a"** tag processes a binary file as if it were text. Manually searched for something that looked like a readable string🤷‍♀️.
