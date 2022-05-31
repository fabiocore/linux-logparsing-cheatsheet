# Linux LOG Parsing Cheat Sheet

## Grep

Grep allows you to search patterns in files. Use ZGREP for GZIP files.

```bash
$ grep <pattern> file.log
```

-n: Number of lines that matches
-i: Case insensitive
-v: Invert matches
-E: Extended regex
-c: Count number of matches
-L: Find filenames that matches the pattern
