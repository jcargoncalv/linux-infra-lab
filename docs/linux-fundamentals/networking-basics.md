# Networking Basics

Networking fundamentals are essential for:

- infrastructure operations
- troubleshooting
- Docker environments
- monitoring systems
- service diagnostics
- remote administration

---

# Viewing Network Interfaces

## Show interfaces and IP addresses

```bash
ip addr
```

Useful for:
- checking connectivity
- identifying local IP addresses
- troubleshooting network configuration

---

# Viewing Routing Information

```bash
ip route
```

Shows:
- default gateway
- routing tables
- network paths

---

# Testing Connectivity

## Ping a host

```bash
ping google.com
```

Useful for:
- connectivity tests
- DNS verification
- latency checks

Stop with:

```bash
Ctrl + C
```

---

# DNS Resolution

## Query DNS records

```bash
nslookup google.com
```

or:

```bash
dig google.com
```

Useful for:
- DNS troubleshooting
- domain resolution checks
- infrastructure diagnostics

---

# Checking Open Ports

## Show listening ports

```bash
ss -tuln
```

Breakdown:

| Option | Meaning |
|---|---|
| `t` | TCP |
| `u` | UDP |
| `l` | listening sockets |
| `n` | numeric output |

Useful for:
- verifying services
- debugging applications
- checking exposed ports

---

# SSH Remote Access

## Connect to a remote server

```bash
ssh user@server-ip
```

Example:

```bash
ssh admin@192.168.1.10
```

SSH is commonly used for:
- server administration
- remote diagnostics
- infrastructure management

---

# File Transfer

## Secure file copy

```bash
scp file.txt user@server:/tmp
```

Useful for:
- deployments
- backups
- transferring logs

---

# Downloading Files

## Using curl

```bash
curl https://example.com
```

## Using wget

```bash
wget https://example.com/file.zip
```

Useful for:
- testing APIs
- downloading artifacts
- operational automation

---

# Checking Network Connections

## Active connections

```bash
ss -tunap
```

Useful for:
- troubleshooting services
- identifying unexpected connections
- monitoring applications

---

# Hostname Information

## Show hostname

```bash
hostname
```

## Show detailed hostname information

```bash
hostnamectl
```

Useful for:
- identifying systems
- operational inventory
- infrastructure diagnostics

---

# Firewall Basics

## UFW status (Ubuntu/Debian)

```bash
sudo ufw status
```

Example:

```bash
sudo ufw allow 22/tcp
```

Useful for:
- securing services
- controlling exposed ports
- infrastructure hardening

---

# Troubleshooting Workflow

Common troubleshooting sequence:

1. Verify interface status
2. Check IP address
3. Test connectivity with `ping`
4. Verify DNS resolution
5. Check listening ports
6. Inspect firewall rules
7. Review service logs

---

# Useful Commands

| Command | Purpose |
|---|---|
| `ip addr` | show interfaces |
| `ip route` | show routes |
| `ping` | connectivity test |
| `dig` | DNS lookup |
| `ss` | socket statistics |
| `ssh` | remote access |
| `scp` | secure copy |
| `curl` | HTTP requests |
| `wget` | file downloads |
| `hostnamectl` | system hostname information |