# Filesystem Fundamentals

## Linux Filesystem Hierarchy

| Directory | Description |
|---|---|
| `/` | Root of the filesystem hierarchy |
| `/home` | User home directories |
| `/etc` | System-wide configuration files |
| `/var` | Variable runtime data, logs, caches |
| `/tmp` | Temporary files |
| `/usr` | User applications and shared resources |
| `/bin` | Essential user binaries |
| `/srv` | Service-specific data |
| `/opt` | Optional or third-party software |

---

## Inspecting Disk Usage

### Disk usage by filesystem

```bash
df -h
```

Useful for:
- diagnosing low disk space
- monitoring mounted filesystems
- checking container volumes

### Directory size analysis

```bash
du -sh *
```

Useful for:
- identifying large directories
- troubleshooting storage growth

---

## File Search

### Find files by name

```bash
find . -name "*.log"
```

### Find recently modified files

```bash
find /var/log -mtime -1
```

Useful during:
- incident analysis
- debugging
- monitoring workflows