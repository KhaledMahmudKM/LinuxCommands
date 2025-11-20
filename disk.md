# Disk and Filesystem Commands

This chapter covers Linux commands for viewing and managing disks, partitions, and filesystems.

---

## 1. `df` — Disk Free Space

**Usage:**

```bash
df -h
```

Options:

* `-h` : human-readable sizes
  Shows total, used, and available space on mounted filesystems.

---

## 2. `du` — Directory Space Usage

**Usage:**

```bash
du -sh /path/to/dir
du -h --max-depth=1 /home
```

Options:

* `-s` : summarize
* `-h` : human-readable
* `--max-depth=N` : limit depth

---

## 3. `lsblk` — List Block Devices

**Usage:**

```bash
lsblk
lsblk -f
```

Shows disks, partitions, and mount points. `-f` shows filesystem info.

---

## 4. `blkid` — Show Filesystem Info

**Usage:**

```bash
blkid /dev/sda1
```

Shows UUID, type, and label of partitions.

---

## 5. `mount` — Mount Filesystems

**Usage:**

```bash
mount /dev/sda1 /mnt
mount -t ext4 /dev/sdb1 /data
```

Mount a device to a directory.

---

## 6. `umount` — Unmount Filesystems

**Usage:**

```bash
umount /mnt
```

Unmount a mounted filesystem.

---

## 7. `fsck` — Check and Repair Filesystem

**Usage:**

```bash
fsck /dev/sda1
```

Checks filesystem consistency and repairs errors.

---

## 8. `mkfs` — Create Filesystem

**Usage:**

```bash
mkfs.ext4 /dev/sdb1
mkfs.xfs /dev/sdb2
```

Creates a new filesystem on a partition.

---

## 9. `parted` — Partition Management

**Usage:**

```bash
parted /dev/sda
(parted) print
(parted) mkpart primary ext4 1MiB 100%
```

Interactive partitioning tool.

---

## 10. `fdisk` — MBR Partitioning Tool

**Usage:**

```bash
fdisk /dev/sda
```

Create, delete, and modify partitions (MBR).

---

## 11. `ls -l /dev/disk/by-uuid/` — View Disk UUIDs

**Usage:**

```bash
ls -l /dev/disk/by-uuid/
```

Shows UUIDs for mounting filesystems in `/etc/fstab`.

---

## 12. `tune2fs` — Tune ext2/ext3/ext4 Filesystem

**Usage:**

```bash
tune2fs -l /dev/sda1
tune2fs -c 30 /dev/sda1  # set max mount count
```

View or modify filesystem parameters.

---

## End of Chapter
