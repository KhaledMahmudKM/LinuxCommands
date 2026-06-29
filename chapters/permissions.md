# File Permissions and Ownership

This chapter covers Linux file permissions, ownership, and commonly used related commands.

---

## 1. Understanding Linux Permissions

Permissions are shown using:

```bash
ls -l
```

Example output:

```bash
-rwxr-xr-- 1 user group 4096 Jan 1  example.sh
```

Breakdown:

* `-` : file type (`d` for directory)
* `rwx` : owner permissions
* `r-x` : group permissions
* `r--` : others permissions

Permission meanings:

* `r` : read
* `w` : write
* `x` : execute

---

## 2. `chmod` — Change File Permissions

**Usage:**

```bash
chmod 755 script.sh
chmod u+x script.sh
chmod g-w file.txt
chmod o-rwx secret.txt
```

Two ways to set permissions:

### Numeric Mode

* `7` = read + write + execute
* `5` = read + execute
* `4` = read only

Example:

```bash
chmod 644 file.txt
```

Owner: read/write, Group: read, Others: read

### Symbolic Mode

```bash
chmod u+r file
chmod g-x file
chmod o-rwx file
```

---

## 3. `chown` — Change File Owner

**Usage:**

```bash
chown user file
chown user:group file
chown -R user:group folder
```

**Description:** Changes the owner or group of a file/directory.

---

## 4. `chgrp` — Change Group Ownership

**Usage:**

```bash
chgrp group file
chgrp -R group folder
```

**Description:** Changes group ownership only.

---

## 5. `umask` — Default Permission Mask

**Usage:**

```bash
umask
umask 022
```

**Description:** Controls default file/folder permissions.

Examples:

* Default file permissions = `666 - umask`
* Default directory permissions = `777 - umask`

If `umask = 022`:

* New files → `644`
* New directories → `755`

---

## 6. Special Permission Bits

Linux supports special modes:

### 1. Setuid (`s`)

```bash
chmod u+s file
```

File runs with the **owner’s privileges**.

### 2. Setgid (`s`)

```bash
chmod g+s directory
```

New files inherit directory group.

### 3. Sticky Bit (`t`)

```bash
chmod +t /shared/dir
```

Only the owner can delete their own files inside the directory.
Common on `/tmp`.

---

## 7. View Ownership and Permissions

**Usage:**

```bash
ls -l
stat file.txt
```

Shows detailed permission and ownership information.

---


