# 🐧 Logs Commands

## View Log Files

| Command | Purpose |
|----------|----------|
| `ls /var/log` | List log files and directories. |
| `cat /var/log/auth.log` | Display the entire log file. |
| `less /var/log/auth.log` | Open a log file and scroll through it. |

---

## Tail Logs

| Command | Purpose |
|----------|----------|
| `tail /var/log/auth.log` | Show the last 10 lines of a log file. |
| `tail -20 /var/log/auth.log` | Show the last 20 lines of a log file. |
| `tail -f /var/log/auth.log` | Monitor a log file in real time. |

---

## Systemd Logs

| Command | Purpose |
|----------|----------|
| `journalctl` | View systemd logs. |
| `journalctl -b` | View logs from the current boot. |
| `journalctl -p err` | Show only error logs. |
| `journalctl -f` | Monitor systemd logs in real time. |
| `journalctl -k` | View kernel logs from systemd. |

---

## Kernel Logs

| Command | Purpose |
|----------|----------|
| `dmesg` | View kernel and hardware messages. |

---

