# Compression and Archiving Commands

This chapter covers Linux commands used to compress, extract, and manage archive files.

---

## 1. `tar` — Archive and Extract Files

**Usage:**

```
tar -cvf archive.tar file1 file2
```

Create an archive:

* `c` : create
* `v` : verbose
* `f` : filename

Extract an archive:

```
tar -xvf archive.tar
```

List contents:

```
tar -tvf archive.tar
```

### Compress with gzip or bzip2

Create gzip-compressed tar:

```
tar -czvf archive.tar.gz folder/
```

Extract:

```
tar -xzvf archive.tar.gz
```

Create bzip2-compressed tar:

```
tar -cjvf archive.tar.bz2 folder/
```

Extract:

```
tar -xjvf archive.tar.bz2
```

---

## 2. `gzip` — Compress Files

**Usage:**

```
gzip file.txt
```

This replaces the file with `file.txt.gz`.

Decompress:

```
gunzip file.txt.gz
```

---

## 3. `bzip2` — High Compression Ratio

**Usage:**

```
bzip2 file.txt
```

Decompress:

```
bunzip2 file.txt.bz2
```

---

## 4. `zip` — Create ZIP Files

**Usage:**

```
zip archive.zip file1 file2
zip -r archive.zip folder/
```

---

## 5. `unzip` — Extract ZIP Files

**Usage:**

```
unzip archive.zip
unzip archive.zip -d folder/
```

---

## 6. `xz` — High-Ratio Compression

**Usage:**

```
xz file.txt
```

Output → `file.txt.xz`

Decompress:

```
unxz file.txt.xz
```

---

## 7. `7z` — 7‑Zip Utility (if installed)

**Usage:**

```
7z a archive.7z folder/
7z x archive.7z
```

Supports many formats: 7z, zip, rar, iso, etc.

---

## 8. Combine Tools

Compress a folder to tar.gz:

```
tar -cvf - folder/ | gzip > folder.tar.gz
```

Extract from tar.gz manually:

```
gzip -dc folder.tar.gz | tar xvf -
```

---

## End of Chapter
