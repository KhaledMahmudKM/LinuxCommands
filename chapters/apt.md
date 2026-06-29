# APT Commands

Search for a package or text string:

```bash
apt search <package/text_string>
```

Show package information:

```bash
apt show <package>
```

Show package dependencies:

```bash
apt depends <package>
```

Show the names of all the packages installed in the system:

```bash
apt list --installed
```

Install a package:

```bash
apt install <package>
```

Uninstall a package:

```bash
apt remove <package>
```

Delete a package including its configuration files:

```bash
apt purge <package>
```

Delete automatically those packages that are not being used (be careful with this command, due to apt's hell dependency it may delete unwanted packages):

```bash
apt autoremove
```

Update the repositories information:

```bash
apt update
```

Update a package to the last available version in the repository:

```bash
apt upgrade <package>
```

Update the full distribution. It will update our system to the next available version:

```bash
sudo parrot-upgrade
```

Clean caches, downloaded packages, etc:

```bash
apt clean && apt autoclean
```


Check the manual page.

```bash
man apt
```

---