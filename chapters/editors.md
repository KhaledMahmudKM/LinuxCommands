# Editors and Viewing Files

This chapter covers Linux text editors and file viewing commands.

---

## 1. `cat` — Concatenate and Display Files

**Usage:**

```bash
cat file.txt
cat file1 file2 > combined.txt
```

Displays file contents or combines files.

---

## 2. `less` — View File Page by Page

**Usage:**

```bash
less file.txt
```

Navigation:

* `Space` : next page
* `b` : previous page
* `q` : quit
* `/pattern` : search

---

## 3. `more` — Simple Pager

**Usage:**

```bash
more file.txt
```

Like `less` but with fewer features.

---

## 4. `nano` — Simple Text Editor

**Usage:**

```bash
nano file.txt
```

Basic editing with on-screen shortcuts.

* `Ctrl+O` : save
* `Ctrl+X` : exit
* `Ctrl+K` : cut line
* `Ctrl+U` : paste line

---

## 5. `vi` / `vim` — Advanced Text Editor

**Usage:**

```bash
vi file.txt
vim file.txt
```

Modes:

* Normal mode : navigation
* Insert mode : editing (`i` to enter)
* Command mode : `:` to run commands

Common commands:

* `:w` : save
* `:q` : quit
* `:wq` : save and quit
* `:q!` : quit without saving
* `/pattern` : search

---

## 6. `head` — View First Lines

**Usage:**

```bash
head file.txt
head -n 20 file.txt
```

Shows top lines of a file.

---

## 7. `tail` — View Last Lines

**Usage:**

```bash
tail file.txt
tail -n 20 file.txt
tail -f logfile.log
```

* `-f` : follow file as it grows

---

## 8. `tac` — Display File in Reverse

**Usage:**

```bash
tac file.txt
```

Displays lines from bottom to top.

---

## 9. `od` — Octal / Hex Dump

**Usage:**

```bash
od -c file.txt
od -x file.bin
```

Displays binary or non-printable data.

---

## 10. `strings` — Extract Printable Strings

**Usage:**

```bash
strings binaryfile
```

Extracts readable strings from binaries or files.

---

