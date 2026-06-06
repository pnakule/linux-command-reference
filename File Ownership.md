
# Linux File Permissions

## View Permissions

| Command | Purpose                                           |
| ------- | ------------------------------------------------- |
| `ls -l` | Display file permissions, owner, group, and size. |


---

## Permission Types

| Symbol | Meaning |
| ------ | ------- |
| `r`    | Read    |
| `w`    | Write   |
| `x`    | Execute |

---

## Permission Groups

| Symbol | Meaning                     |
| ------ | --------------------------- |
| `u`    | User / Owner                |
| `g`    | Group                       |
| `o`    | Others                      |
| `a`    | All (User + Group + Others) |

---

## Change Permissions

| Command              | Purpose                              |
| -------------------- | ------------------------------------ |
| `chmod u+x file name` | Give execute permission to owner.    |
| `chmod g-w file name` | Remove write permission from group.  |
| `chmod o+r file name` | Give read permission to others.      |
| `chmod a+x file name` | Give execute permission to everyone. |

---

## Numeric Permissions

| Value | Permission    |
| ----- | ------------- |
| `4`   | Read (`r`)    |
| `2`   | Write (`w`)   |
| `1`   | Execute (`x`) |

---

## Common Permission Values

| Number | Permission |
| ------ | ---------- |
| `7`    | `rwx`      |
| `6`    | `rw-`      |
| `5`    | `r-x`      |
| `4`    | `r--`      |
| `0`    | `---`      |

---

## Common chmod Examples

| Command              | Purpose                                         |
| -------------------- | ----------------------------------------------- |
| `chmod 777 file name` | Full permissions for everyone.                  |
| `chmod 755 file name` | Full access for owner, read/execute for others. |
| `chmod 644 file name` | Read/write for owner, read-only for others.     |
| `chmod 600 file name` | Read/write for owner only.                      |
| `chmod 700 file name` | Full access for owner only.                     |

---

## Understanding chmod Numbers

### chmod 777

```text
User   = 7 = rwx
Group  = 7 = rwx
Others = 7 = rwx
```

---

### chmod 755

```text
User   = 7 = rwx
Group  = 5 = r-x
Others = 5 = r-x
```

---

### chmod 644

```text
User   = 6 = rw-
Group  = 4 = r--
Others = 4 = r--
```

---

## Change Ownership

| Command                                | Purpose                      |
| -------------------------------------- | ---------------------------- |
| `sudo chown user-name file name`            | Change file owner.           |
| `sudo chown user-name:group-name file name` | Change file owner and group. |

---

## Change Group

| Command                          | Purpose            |
| -------------------------------- | ------------------ |
| `sudo chgrp group-name file name` | Change file group. |

---

## Group Management

| Command                             | Purpose                |
| ----------------------------------- | ---------------------- |
| `sudo groupadd group-name`          | Create a new group.    |
| `sudo usermod -aG group-name user-name` | Add user to a group.   |
| `groups user-name`                      | Show groups of a user. |

---

## Directory Permissions

| Permission | Meaning                              |
| ---------- | ------------------------------------ |
| `r`        | List files in directory.             |
| `w`        | Create or delete files in directory. |
| `x`        | Enter the directory using `cd`.      |

---

## Reading ls -l Output

Example:

```text
-rw-r--r-- 1 user1 developers 0 Jun 6 11:27 file.txt
```

| Field        | Meaning           |
| ------------ | ----------------- |
| `-rw-r--r--` | Permissions       |
| `1`          | Link count        |
| `user1`      | Owner             |
| `developers` | Group             |
| `0`          | File size (bytes) |
| `file.txt`   | File name         |

---

## Change Permissions on Multiple Files

| Command                       | Purpose                                                          |
| ----------------------------- | ---------------------------------------------------------------- |
| `chmod 644 file1 file2 file3` | Change permissions for multiple files.                           |
| `chmod 644 *`                 | Change permissions for all files in current directory.           |
| `chmod +x *.sh`               | Make all shell scripts executable.                               |
| `chmod -R 755 directory/`     | Change permissions recursively for a directory and its contents. |


