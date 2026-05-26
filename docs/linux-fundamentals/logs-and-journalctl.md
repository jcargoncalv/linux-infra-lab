# Logs and Journalctl

## System Logs

Important Files:

| Path | Purpose |
|---|---|
| /var/log/syslog | general system logs |
| /var/log/auth.log | authentication logs |
| /var/log/kern.log | kernel logs |

---

## View Recent Logs

```bash
journalctl -n 50
```

---

## Follow Logs in Real Time

```bash
journalctl -f
```

Equivalent to:

```bash
tail -f logfile.log
```

---

## Logs for a Specific Service

```bash
journalctl -u docker
```

Useful for:
- troubleshooting containers
- diagnosing startup failures
- operational monitoring