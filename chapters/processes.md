# Process Management Commands

This chapter covers commands for viewing, controlling, and managing processes in Linux.

---

## 1. `ps` — Show Running Processes

**Usage:**

```bash
ps
ps aux
ps -ef
```

**Description:** Lists active processes.

Common formats:

* `ps aux` : BSD style
* `ps -ef` : Unix style (more common in scripting)

Filter by name:

```bash
ps aux | grep nginx
```

---

## 2. `top` — Real-Time Process Viewer

**Usage:**

```bash
top
```

**Description:** Shows CPU, memory usage, and running processes interactively.

Navigation:

* `q` : quit
* `k` : kill a process
* `h` : help

---

## 3. `htop` — Enhanced Process Viewer

**Usage:**

```bash
htop
```

**Description:** More user-friendly version of `top` with color and interactive controls.
(May need to be installed.)

---

## 4. `pidof` — Get PID of a Process

**Usage:**

```bash
pidof sshd
```

**Description:** Shows the process ID (PID) of a program.

---

## 5. `pgrep` / `pkill` — Search or Kill by Name

**Usage:**

```bash
pgrep ssh
pkill ssh
```

**Description:**

* `pgrep` finds PIDs by name/pattern
* `pkill` kills processes by name/pattern

---

## 6. `kill` — Terminate a Process by PID

**Usage:**

```bash
kill 1234
kill -9 1234
```

**Description:** Sends a signal to a process.

Common signals:

* `15` (TERM) : safe terminate (default)
* `9` (KILL) : force kill

---

## 7. `killall` — Kill Multiple Processes by Name

**Usage:**

```bash
killall firefox
```

---

## 8. `nice` — Start Program with Priority

**Usage:**

```bash
nice -n 10 myscript.sh
```

**Description:** Lower priority = negative values; higher priority = positive.
Range: `-20` (highest priority) → `19` (lowest priority)

---

## 9. `renice` — Change Priority of Existing Process

**Usage:**

```bash
renice 5 -p 1234
```

**Description:** Adjusts the scheduling priority of a running process.

---

## 10. `systemctl` — Manage Services (systemd)

**Usage:**

```bash
systemctl status nginx
systemctl start nginx
systemctl stop nginx
systemctl enable nginx
systemctl disable nginx
```

**Description:** Controls systemd-based services.

---

## 11. `service` — Legacy Service Control

**Usage:**

```bash
service apache2 status
service ssh restart
```

---

## 12. `jobs`, `bg`, `fg` — Shell Job Control

### Background jobs:

```bash
command &
```

View jobs:

```bash
jobs
```

Move job to background:

```bash
bg %1
```

Bring job to foreground:

```bash
fg %1
```

---

## 13. `nohup` — Run Command Immune to Hangups

**Usage:**

```bash
nohup myscript.sh &
```

**Description:** Keeps a command running after logout.

Creates `nohup.out` unless redirected.

---

## 14. `strace` — Trace System Calls

**Usage:**

```bash
strace ls
strace -p 1234
```

**Description:** Debugging and troubleshooting tool for tracking system calls.

---


