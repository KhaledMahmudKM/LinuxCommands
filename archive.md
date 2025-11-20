# Compression and Archiving Commands

This chapter covers Linux commands used to compress, extract, and manage archive files.

---

## 1. `tar` — Archive and Extract Files

**Usage:**

```bash
tar -cvf archive.tar file1 file2
```

Create an archive:

* `c` : create
* `v` : verbose
* `f` : filename

Extract an archive:

```bash
tar -xvf archive.tar
```

List contents:

```bash
tar -tvf archive.tar
```

### Compress with gzip or bzip2

Create gzip-compressed tar:

```bash
tar -czvf archive.tar.gz folder/
```

Extract:

```bash
tar -xzvf archive.tar.gz
```

Create bzip2-compressed tar:

```bash
tar -cjvf archive.tar.bz2 folder/
```

Extract:

```bash
tar -xjvf archive.tar.bz2
```

---

## 2. `gzip` — Compress Files

**Usage:**

```bash
gzip file.txt
```

This replaces the file with `file.txt.gz`.

Decompress:

```bash
gunzip file.txt.gz
```

---

## 3. `bzip2` — High Compression Ratio

**Usage:**

```bash
bzip2 file.txt
```

Decompress:

```bash
bunzip2 file.txt.bz2
```

---

## 4. `zip` — Create ZIP Files

**Usage:**

```bash
zip archive.zip file1 file2
zip -r archive.zip folder/
```

---

## 5. `unzip` — Extract ZIP Files

**Usage:**

```bash
unzip archive.zip
unzip archive.zip -d folder/
```

---

## 6. `xz` — High-Ratio Compression

**Usage:**

```bash
xz file.txt
```

Output → `file.txt.xz`

Decompress:

```bash
unxz file.txt.xz
```

---

## 7. `7z` — 7‑Zip Utility (if installed)

**Usage:**

```bash
7z a archive.7z folder/
7z x archive.7z
```

Supports many formats: 7z, zip, rar, iso, etc.

---

## 8. Combine Tools

Compress a folder to tar.gz:

```bash
tar -cvf - folder/ | gzip > folder.tar.gz
```

Extract from tar.gz manually:

```bash
gzip -dc folder.tar.gz | tar xvf -
```

---

## End of Chapter
