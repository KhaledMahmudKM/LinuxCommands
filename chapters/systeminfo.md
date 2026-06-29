# System Information Commands

This chapter covers Linux commands to view system information, hardware details, and performance metrics.

---

## 1. `uname` — System Information

**Usage:**

```bash
uname -a
uname -r
uname -m
```

Options:

* `-a` : all info
* `-r` : kernel version
* `-m` : architecture

---

## 2. `hostnamectl` — View and Change Hostname

**Usage:**

```bash
hostnamectl
hostnamectl set-hostname newname
```

---

## 3. `uptime` — System Uptime

**Usage:**

```bash
uptime
```

Shows how long the system has been running, users logged in, load averages.

---

## 4. `dmesg` — Kernel Messages

**Usage:**

```bash
dmesg | less
```

**Description:** Shows kernel ring buffer messages, useful for hardware issues.

---

## 5. `lscpu` — CPU Information

**Usage:**

```bash
lscpu
```

Shows number of cores, threads, architecture, CPU family, model, cache size.

---

## 6. `lsblk` — Block Devices

**Usage:**

```bash
lsblk
lsblk -f
```

Shows disks, partitions, mount points, and filesystem types.

---

## 7. `lspci` — PCI Devices

**Usage:**

```bash
lspci
lspci -v
```

Shows hardware connected via PCI (network cards, GPUs, etc.).

---

## 8. `lsusb` — USB Devices

**Usage:**

```bash
lsusb
lsusb -v
```

Shows connected USB devices.

---

## 9. `free` — Memory Usage

**Usage:**

```bash
free -h
```

Options:

* `-h` : human-readable sizes
  Shows total, used, free memory and swap.

---

## 10. `vmstat` — Virtual Memory Statistics

**Usage:**

```bash
vmstat 1
```

Shows CPU, memory, I/O, system statistics in real-time.

---

## 11. `df` — Disk Usage

**Usage:**

```bash
df -h
```

Shows available, used, and total space for mounted filesystems.

---

## 12. `du` — Directory Space Usage

**Usage:**

```bash
du -sh /path/to/dir
du -h --max-depth=1 /home
```

---

## 13. `top` / `htop` — Resource Usage

**Usage:**

```bash
top
htop
```

Shows CPU, memory, and process usage in real-time.

---

## 14. `uptime` and `w` — Logged-in Users

**Usage:**

```bash
uptime
w
```

Shows users currently logged in and system load.

---

