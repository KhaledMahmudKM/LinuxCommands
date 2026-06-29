# Networking Commands

This chapter covers essential Linux networking commands used for checking connections, interfaces, routing, DNS, and troubleshooting.

---

## 1. `ip` — Manage Network Interfaces, Routes, and More

**Usage:**

```bash
ip a          # show interfaces
ip link       # show link layer info
ip r          # show route table
ip neigh      # show ARP table
```

Common tasks:

```bash
ip addr add 192.168.1.10/24 dev eth0
ip link set eth0 up
ip route add default via 192.168.1.1
```

---

## 2. `ifconfig` — Legacy Interface Viewer

**Usage:**

```bash
ifconfig
ifconfig eth0 up
```

**Note:** Deprecated. Use `ip` instead.

---

## 3. `ping` — Test Connectivity

**Usage:**

```bash
ping google.com
ping -c 4 8.8.8.8
```

Tests if a host is reachable.

---

## 4. `traceroute` — Trace Network Path

**Usage:**

```bash
traceroute google.com
```

Shows each hop from your system to the destination.

---

## 5. `tracepath` — Alternative Path Tracing Tool

**Usage:**

```bash
tracepath google.com
```

Does not require root privileges.

---

## 6. `netstat` — Show Ports, Connections, Routing Table

**Usage:**

```bash
netstat -tulnp
netstat -an
```

**Options:**

* `-t` : TCP
* `-u` : UDP
* `-l` : listening ports
* `-n` : numeric output
* `-p` : show processes

**Note:** Deprecated in favor of `ss`.

---

## 7. `ss` — Modern Socket Viewer

**Usage:**

```bash
ss -tulnp
ss -s
```

Shows active connections, ports, and statistics.

---

## 8. `curl` — Send HTTP Requests

**Usage:**

```bash
curl https://example.com
curl -I https://example.com   # headers only
```

Download file:

```bash
curl -O https://example.com/file.zip
```

---

## 9. `wget` — Download Files from the Web

**Usage:**

```bash
wget https://example.com/file.iso
wget -c file.iso   # resume download
```

---

## 10. `dig` — DNS Lookup

**Usage:**

```bash
dig google.com
```

Query specific DNS record:

```bash
dig A example.com
```

Use specific DNS server:

```bash
dig @8.8.8.8 example.com
```

---

## 11. `nslookup` — Simple DNS Query Tool

**Usage:**

```bash
nslookup example.com
```

---

## 12. `host` — DNS Lookup Utility

**Usage:**

```bash
host example.com
```

---

## 13. `nmcli` — Network Manager CLI

**Usage:**

```bash
nmcli device status
nmcli connection show
nmcli device connect eth0
```

Manage network settings programmatically.

---

## 14. `arp` — Show ARP Cache

**Usage:**

```bash
arp -a
```

**Note:** Newer systems use `ip neigh`.

---

## 15. `ethtool` — NIC Configuration Viewer

**Usage:**

```bash
ethtool eth0
```

Shows link speed, duplex, driver info.

---

## 16. `tcpdump` — Packet Sniffer

**Usage:**

```bash
tcpdump -i eth0
```

Capture packets to file:

```bash
tcpdump -i eth0 -w capture.pcap
```

---

## 17. `nmap` — Network Scanner

**Usage:**

```bash
nmap 192.168.1.0/24
nmap -sV target
```

Scans open ports, services, OS fingerprinting.

---

## 18. `hostname` — View or Set Hostname

**Usage:**

```bash
hostname
hostname newname
```

---

## 19. `whois` — Domain Information Lookup

**Usage:**

```bash
whois example.com
```

---

## 20. `ipcalc` - IP Address Calculator

**Usage:**

```bash
ipcalc 192.168.1.5/24
```

Shows network, broadcast, usable range, etc.

---


