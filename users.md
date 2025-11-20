# User and Group Management Commands

This chapter covers Linux commands to manage users, groups, and their permissions.

---

## 1. `who` — Show Logged-in Users

**Usage:**

```
who
```

Displays currently logged-in users.

---

## 2. `w` — Users and System Activity

**Usage:**

```
w
```

Shows logged-in users, their processes, and system load.

---

## 3. `id` — Show User Identity

**Usage:**

```
id username
id
```

Displays UID, GID, and group memberships.

---

## 4. `groups` — Show Group Membership

**Usage:**

```
groups username
groups
```

Lists groups a user belongs to.

---

## 5. `whoami` — Current User

**Usage:**

```
whoami
```

Displays the username of the current session.

---

## 6. `useradd` — Add a New User

**Usage:**

```
sudo useradd -m username
sudo useradd -M username  # no home directory
sudo useradd -s /bin/bash username
```

Options:

* `-m` : create home directory
* `-s` : set shell

---

## 7. `passwd` — Set or Change Password

**Usage:**

```
sudo passwd username
passwd
```

Prompts for a new password.

---

## 8. `usermod` — Modify User

**Usage:**

```
sudo usermod -aG group username  # add to group
sudo usermod -L username          # lock account
sudo usermod -s /bin/sh username  # change shell
```

---

## 9. `userdel` — Delete User

**Usage:**

```
sudo userdel username
sudo userdel -r username   # remove home directory
```

---

## 10. `groupadd` — Create Group

**Usage:**

```
sudo groupadd groupname
```

---

## 11. `groupdel` — Delete Group

**Usage:**

```
sudo groupdel groupname
```

---

## 12. `gpasswd` — Manage Group Password

**Usage:**

```
gpasswd -a username group   # add user to group
```

---

## 13. `chage` — Password Expiry Info

**Usage:**

```
chage -l username
```

Shows password expiry, minimum/maximum age, warning period.

---

## 14. `getent` — Get Entries from Databases

**Usage:**

```
getent passwd
getent group
```

View users and groups from system databases.

---

## End of Chapter
