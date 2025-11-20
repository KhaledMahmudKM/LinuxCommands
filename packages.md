# Package Management Commands

This chapter covers Linux package management commands for installing, updating, and removing software.

---

## 1. `apt` — Debian/Ubuntu Package Manager

**Usage:**
bash
```
sudo apt update          # refresh package lists
sudo apt upgrade         # upgrade installed packages
sudo apt install pkgname # install a package
sudo apt remove pkgname  # remove a package
sudo apt autoremove      # remove unused dependencies
```

---

## 2. `dpkg` — Debian Package Tool

**Usage:**

```bash
dpkg -i package.deb      # install .deb file
dpkg -r pkgname          # remove package
dpkg -l                  # list installed packages
dpkg -L pkgname          # list files of a package
dpkg -s pkgname          # package status
```

---

## 3. `yum` — RHEL/CentOS Package Manager

**Usage:**

```bash
sudo yum install pkgname
sudo yum remove pkgname
sudo yum update
sudo yum list installed
sudo yum search keyword
```

---

## 4. `dnf` — Fedora Package Manager

**Usage:**

```bash
sudo dnf install pkgname
sudo dnf remove pkgname
sudo dnf update
sudo dnf list installed
sudo dnf search keyword
```

---

## 5. `rpm` — Red Hat Package Tool

**Usage:**

```bash
rpm -i package.rpm      # install package
rpm -e pkgname          # remove package
rpm -qa                 # list installed packages
rpm -ql pkgname         # list files in a package
```

---

## 6. `snap` — Universal Linux Packages

**Usage:**

```bash
sudo snap install pkgname
sudo snap remove pkgname
snap list                 # list installed snaps
snap info pkgname         # show package details
```

---

## 7. `flatpak` — Cross-Distro Packages

**Usage:**

```bash
flatpak install flathub pkgname
flatpak uninstall pkgname
flatpak list
flatpak info pkgname
```

---

## 8. `brew` — Linuxbrew/Homebrew (Optional)

**Usage:**

```bash
brew install pkgname
brew uninstall pkgname
brew update
brew upgrade
brew list
```

---

## End of Chapter
