# Linux Users & Groups

## Check Current User

| Command  | Purpose                                             |
| -------- | --------------------------------------------------- |
| `whoami` | Show the current logged-in username.                |
| `id`     | Show user ID, primary group, and group memberships. |

---

## Sudo & Root

| Command        | Purpose                              |
| -------------- | ------------------------------------ |
| `sudo command` | Run a single command as root.        |
| `sudo su`      | Switch to the root user.             |
| `exit`         | Return to the previous user session. |

---

## Create Users

| Command                    | Purpose                               |
| -------------------------- | ------------------------------------- |
| `sudo useradd username`    | Create a new user account.            |
| `sudo useradd -m username` | Create a user and its home directory. |

---

## Password Management

| Command                | Purpose                                |
| ---------------------- | -------------------------------------- |
| `passwd`               | Change your own password.              |
| `sudo passwd username` | Set or change another user's password. |

---

## Switch Users

| Command              | Purpose                                    |
| -------------------- | ------------------------------------------ |
| `su username`        | Switch to another user.                    |
| `sudo su - username` | Switch to another user with a login shell. |
| `exit`               | Return to the previous user.               |

---

## Delete Users

| Command                    | Purpose                                   |
| -------------------------- | ----------------------------------------- |
| `sudo userdel username`    | Delete a user account only.               |
| `sudo userdel -r username` | Delete a user account and home directory. |

---

## Home Directories

| Command                     | Purpose                                                 |
| --------------------------- | ------------------------------------------------------- |
| `echo $HOME`                | Show your home directory path.                          |
| `grep username /etc/passwd` | Show a user's account details including home directory. |

---

## View Users

| Command                                       | Purpose                                  |
| --------------------------------------------- | ---------------------------------------- |
| `cat /etc/passwd`                             | Show all user accounts.                  |
| `cut -d: -f1 /etc/passwd`                     | Show only usernames.                     |
| `awk -F: '$3 >= 1000 {print $1}' /etc/passwd` | Show normal users (UID 1000+).           |
| `who`                                         | Show currently logged-in users.          |
| `w`                                           | Show logged-in users and their activity. |

---

## Modify Users

| Command                               | Purpose                       |
| ------------------------------------- | ----------------------------- |
| `sudo usermod -aG sudo username`      | Add a user to the sudo group. |
| `sudo usermod -aG groupname username` | Add a user to a group.        |
| `sudo usermod -l newname oldname`     | Rename a user account.        |

---

## Groups

| Command                   | Purpose                          |
| ------------------------- | -------------------------------- |
| `sudo groupadd groupname` | Create a new group.              |
| `groups`                  | Show groups of the current user. |
| `groups username`         | Show groups of a specific user.  |
| `cat /etc/group`          | Show all groups on the system.   |

---

## Key Concepts

| Term           | Meaning                                        |
| -------------- | ---------------------------------------------- |
| UID            | Unique numeric ID of a user.                   |
| GID            | Primary group ID of a user.                    |
| Group          | Collection of users sharing permissions.       |
| Home Directory | User's personal working directory.             |
| Root User      | Administrative user with highest privileges.   |
| Sudo Group     | Users allowed to perform administrative tasks. |

---

## Permission Flow

```text
User → Group → Permissions
```

Example:

```text
itachi → sudo → Administrative Privileges
```
