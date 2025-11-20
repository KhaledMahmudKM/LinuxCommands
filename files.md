# File and Directory Commands

This chapter covers common Linux commands for working with files and directories.

---

## 1. `ls` — List Files and Directories

**Usage:**

```
ls
ls -l
ls -a
ls -lh
```

**Description:** Lists directory contents.

* `-l` : long format
* `-a` : show hidden files
* `-h` : human-readable sizes

---

## 2. `cd` — Change Directory

**Usage:**

```
cd /path/to/dir
cd ..
cd ~
```

**Description:** Moves between directories.

---

## 3. `pwd` — Print Working Directory

**Usage:**

```
pwd
```

**Description:** Shows your current directory path.

---

## 4. `mkdir` — Create Directory

**Usage:**

```
mkdir new_folder
mkdir -p parent/child
```

**Description:** Creates one or more directories.

* `-p` : create parent directories as needed

---

## 5. `rmdir` — Remove Empty Directory

**Usage:**

```
rmdir folder
```

**Description:** Removes a directory **only if it is empty**.

---

## 6. `rm` — Remove Files or Directories

**Usage:**

```
rm file.txt
rm -r folder
rm -rf folder
```

**Description:** Deletes files or directories.

* `-r` : recursive delete
* `-f` : force delete

⚠️ *Be careful with `rm -rf`.*

---

## 7. `cp` — Copy Files or Directories

**Usage:**

```
cp source.txt dest.txt
cp -r source_dir dest_dir
```

**Description:** Copies files or directories.

* `-r` : copy recursively

---

## 8. `mv` — Move or Rename Files

**Usage:**

```
mv old.txt new.txt
mv file.txt /path/to/dir/
```

**Description:** Moves or renames files and directories.

---

## 9. `touch` — Create Empty File / Update Timestamp

**Usage:**

```
touch file.txt
```

**Description:** Creates a blank file or updates the timestamp of an existing file.

---

## 10. `cat` — View File Contents

**Usage:**

```
cat file.txt
```

**Description:** Displays file contents.

---

## 11. `head` & `tail` — Show Beginning / End of File

**Usage:**

```
head file.txt
head -n 20 file.txt

tail file.txt
tail -f logfile.log
```

**Description:**

* `head` shows the first lines
* `tail` shows the last lines
* `tail -f` follows updates in real time

---

## 12. `stat` — Detailed File Info

**Usage:**

```
stat file.txt
```

**Description:** Shows size, permissions, timestamps, inode info.

---

## 13. `file` — Show File Type

**Usage:**

```
file file.txt
```

**Description:** Identifies file type (text, binary, image, etc.).

---

## End of Chapter
