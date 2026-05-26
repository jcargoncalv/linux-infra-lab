# Permissions and Ownership

Linux permissions control who can:

- read files
- modify files
- execute programs
- access directories

Understanding permissions is essential for:

- system administration
- security
- automation
- service management
- troubleshooting

---

# Viewing Permissions

Use:

```bash
ls -l
```

Example:

```text
-rwxr-xr-- 1 user developers 4096 May 26 script.sh
```

---

# Permission Structure

```text
-rwxr-xr--
```

Breakdown:

| Section | Meaning |
|---|---|
| `-` | file type |
| `rwx` | owner permissions |
| `r-x` | group permissions |
| `r--` | others permissions |

---

# Permission Types

| Symbol | Meaning |
|---|---|
| `r` | read |
| `w` | write |
| `x` | execute |

---

# Numeric Permission Values

| Permission | Value |
|---|---|
| `r` | 4 |
| `w` | 2 |
| `x` | 1 |

Examples:

| Numeric | Meaning |
|---|---|
| `755` | owner full access, others read/execute |
| `644` | owner read/write, others read-only |
| `700` | owner only access |

---

# Changing Permissions

## Using chmod

### Make a script executable

```bash
chmod +x script.sh
```

### Set permissions numerically

```bash
chmod 755 script.sh
```

Useful for:
- deployment scripts
- automation tooling
- operational utilities

---

# Changing Ownership

## Using chown

```bash
sudo chown user:group file.txt
```

Example:

```bash
sudo chown nginx:nginx /var/www/html
```

Useful for:
- web servers
- service management
- containerized environments

---

# Directory Permissions

Directories use permissions differently:

| Permission | Directory Meaning |
|---|---|
| `r` | list directory contents |
| `w` | create/delete files |
| `x` | enter/access directory |

---

# Common Operational Examples

## Secure a private SSH key

```bash
chmod 600 ~/.ssh/id_rsa
```

---

## Make a deployment script executable

```bash
chmod +x deploy.sh
```

---

## Restrict access to sensitive files

```bash
chmod 700 secrets/
```

---

# Sudo and Administrative Access

Use `sudo` to execute commands with elevated privileges:

```bash
sudo systemctl restart nginx
```

Be careful when operating as root because system-wide changes can affect services, permissions, and security.

---

# Best Practices

- use least-privilege access
- avoid unnecessary `777` permissions
- restrict sensitive configuration files
- verify ownership after deployments
- use groups for shared access management

---

# Useful Commands

| Command | Purpose |
|---|---|
| `ls -l` | view permissions |
| `chmod` | change permissions |
| `chown` | change ownership |
| `groups` | show user groups |
| `whoami` | current user |
| `id` | user and group information |