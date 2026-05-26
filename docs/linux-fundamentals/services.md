# Systemd Services

## Check Service Status

```bash
systemctl status nginx
```

---

## Start / Stop Services

```bash
sudo systemctl start nginx
sudo systemctl stop nginx
```

---

## Enable Service at Boot

```bash
sudo systemctl enable nginx
```

---

## View Service Logs

```bash
journalctl -u nginx
```

Useful for:
- troubleshooting startup failures
- debugging service crashes
- operational diagnostics