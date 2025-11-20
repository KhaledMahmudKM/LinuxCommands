# Error Logs and Troubleshooting Commands

This chapter covers Linux commands and locations for viewing system and application error logs for troubleshooting purposes.

---

## 1. `journalctl` — Systemd Journal Logs

**Usage:**

```bash
journalctl             # view all logs
journalctl -u service   # logs for a specific service
journalctl -f           # follow logs in real-time
journalctl -p err       # show only error logs
```

---

## 2. `dmesg` — Kernel and Boot Messages

**Usage:**

```bash
dmesg                   # view kernel messages
dmesg | less
```

Useful for hardware or boot-related errors.

---

## 3. `/var/log/` — Log File Directory

**Common Logs:**

```bash
/var/log/syslog         # general system messages (Debian/Ubuntu)
/var/log/messages       # general messages (RHEL/CentOS)
/var/log/auth.log       # authentication logs
/var/log/kern.log       # kernel logs
/var/log/dmesg          # boot and kernel messages
/var/log/boot.log       # boot logs
/var/log/apache2/       # Apache web server logs
/var/log/nginx/         # Nginx logs
/var/log/mysql/         # MySQL/MariaDB logs
```

View log files:

```bash
less /var/log/syslog
cat /var/log/auth.log
```

---

## 4. `tail` — View Recent Log Entries

**Usage:**

```bash
tail /var/log/syslog
tail -n 50 /var/log/syslog
```

Follow logs in real-time:

```bash
tail -f /var/log/syslog
```

---

## 5. `grep` — Search Logs

**Usage:**

```bash
grep "error" /var/log/syslog
grep -i "fail" /var/log/auth.log
```

Combine with `tail` for live monitoring:

```bash
tail -f /var/log/syslog | grep error
```

---

## 6. `logger` — Add Custom Log Entries

**Usage:**

```bash
logger "This is a test log message"
```

Adds a message to the system log.

---

## 7. `watch` — Monitor Logs or Commands

**Usage:**

```bash
watch -n 2 tail -n 20 /var/log/syslog
```

Run a command repeatedly every few seconds.

---

## End of Chapter
