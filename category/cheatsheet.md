---
layout: category
title: Resources & CheatSheets
---

This is a quick & dirty cheatsheet for me and others

---

# Linux 
<br />
<br />

## Terminal

### grep
**_lets you search files for text_**

ex:

```md
    $ grep something filename.txt
```
-i: case-insensitive

-A, -B: show context $grep -A 3 foo shows 3 lines of context after
match. (A - after, B - before, C - Center)

-E: regex, or type egrep

-v: invert matches, find all lines that do not match

-l: only show filenames of matches

-F: don't treat the match string as regex

-r: recursive

-o: only print matching part of the line

--include \\*.filetype: allows wildcard matching for filetypes (alternatively: --include="")

or for multiple filetypes:

```md
grep --include=*.{py,md,in} 'filename'
```

### xargs

**_takes lines from stdin and convert them into cmd args_**

ex:
```md

    #echo "/home /tmp" | xargs ls
```

will run

```md
    ls /home /tmp
```

this is useful when you want to run the same commands on a list of files.
(xargs rm, cat, grep, sed)

replace foo with bar in all text files:

```md
    find . -name '*.txt' | xargs sed -i s/foo/bar/g
```

-n 1: makes xargs run a seperate program for every input
-P: max numberof parallel processes xargs will start

### find

**_yeah kinda self-explanatory_**

ex:
```md
    find . -name \*.zip
```
### other

