# Searching and Filtering Commands

This chapter covers Linux commands used to search for files, search inside files, and filter text.

---

## 1. `find` — Search for Files and Directories

**Usage:**

```
find /path -name "file.txt"
find /path -type f -size +10M
find . -mtime -1
find . -user username
find / -perm 644
```

**Common Options:**

* `-name` : search by name
* `-type f/d` : file or directory
* `-size` : size (+10M = greater than 10MB)
* `-mtime` : modified time in days
* `-perm` : permission
* `-user` : owner

### Run a command on matches

```
find . -name "*.log" -exec rm {} \;
```

Deletes all `.log` files.

---

## 2. `locate` — Fast File Search

**Usage:**

```
locate file.txt
locate *.conf
```

**Description:** Searches using a database (`updatedb`).

Update database manually:

```
sudo updatedb
```

---

## 3. `grep` — Search Text Inside Files

**Usage:**

```
grep "hello" file.txt
grep -i "error" file.txt
grep -r "keyword" /path
```

**Options:**

* `-i` : ignore case
* `-r` : recursive
* `-n` : show line numbers
* `-v` : invert match (show lines *not* matching)

Example with highlighting:

```
grep --color=auto "pattern" file.txt
```

---

## 4. `egrep` and `fgrep`

* `egrep` = `grep -E` (extended regex)
* `fgrep` = `grep -F` (fixed strings, no regex)

Examples:

```
egrep "cat|dog" pets.txt
fgrep "hello*world" file.txt   # literal text
```

---

## 5. `awk` — Pattern Scanning and Processing

**Usage:**

```
awk '{print $1}' file.txt
awk '/error/ {print $0}' logfile
awk -F: '{print $1,$3}' /etc/passwd
```

**Description:** A powerful tool for filtering and formatting text.

Common uses:

* Print specific columns
* Match patterns
* Process delimited files

---

## 6. `sed` — Stream Editor

**Usage:**

```
sed 's/old/new/' file.txt
sed -i 's/foo/bar/g' file.txt
sed -n '1,10p' file.txt
```

**Description:** For modifying text from input streams or files.

Common actions:

* Replace text
* Delete lines
* Print specific ranges

---

## 7. `wc` — Word, Line, and Byte Count

**Usage:**

```
wc file.txt
wc -l file.txt   # lines
wc -w file.txt   # words
wc -c file.txt   # bytes
```

---

## 8. `sort` — Sort Text

**Usage:**

```
sort file.txt
sort -n numbers.txt
sort -r file.txt
sort -u file.txt
```

**Options:**

* `-n` : numeric sort
* `-r` : reverse sort
* `-u` : unique

---

## 9. `uniq` — Filter Unique or Duplicate Lines

**Usage:**

```
uniq file.txt
uniq -c file.txt  # count duplicates
uniq -d file.txt  # only duplicates
```

Tip: Use with sort:

```
sort file.txt | uniq -c
```

---

## 10. `cut` — Extract Columns

**Usage:**

```
cut -d ':' -f 1 /etc/passwd
cut -c 1-10 file.txt
```

**Options:**

* `-d` : delimiter
* `-f` : select fields
* `-c` : character position

---

## 11. Combine Commands Using Pipes

**Usage:**

```
ps aux | grep python
cat logfile | grep error | wc -l
```

**Description:** Pipes (`|`) pass output of one command into another.

---

## End of Chapter
