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

## Level 6 -> Level 7
