# Linux LOG Parsing Cheat Sheet

## GREP

GREP allows you to search patterns in files. Use ZGREP for GZIP files.

```bash
$ grep <pattern> file.log
```

-n: Number of lines that matches

-i: Case insensitive

-v: Invert matches

-E: Extended regex

-c: Count number of matches

-I: Find filenames that matches the pattern

# NGREP

NGREP is used for analyzing network packets.

```bash
$ ngrep -I file.pcap
```

-d: Specify network interface

-i: Case insensitive

-x: Print in alternate hexdump

-t: Print timestamp

-I: Read pcap file

# CUT

The CUT command is used to parse fields from delimited logs.

```bash
$ cut -d "." -f 2 file.log
```

-d: Use the field delimiter

-f: The field numbers

-c: Specifies characters position

# SED

SED (Stream Editor) is used to replace strings in a file.

```bash
$ sed /s/regex/replace/g
```

s: Search

g: Replace

d: Delete

w: Append to file

-e: Execute command

-n: Suppress output

# SORT

SORT is used to sort a file.

```bash
$ sort foo.txt
```

-o: Output to file

-r: Reverse order

-n: Numerical sort

-k: Sort by column.

-c: Check if ordered

-u: Sort and remove

-f: Ignore case

-h: Human sort

# UNIQ

UNIQ is used to extract uniq occurrences.

```bash
$ uniq foo.txt
```

-c: Count the number of duplicates

-d: Print duplicates

-i: Case insensitive

# DIFF

DIFF is used to display differences in files by comparing line by line.

```bash
diff foo.log bar.log
```

How to read the output?

a: Add

c: Change

d: Delete

#: Line numbers

\<: File 1

\>: File 2

# AWK

AWK is a programming language used to manipulate data.

```bash
$ aws { print $2} foo.log
```

Print first column with separator "."

```bash
$ awk -F: '{print $|}' /etc/password
```

Extract uniq value from two files

```bash
$ awk 'FNR==NR { a[$O]++; next} |($O in a)' file1.txt file2.txt
```
