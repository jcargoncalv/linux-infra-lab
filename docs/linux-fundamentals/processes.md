# Processes and System Monitoring

## Viewing Running Processes

```bash
ps aux
```

Important fields:
- PID
- CPU usage
- memory usage
- command

---

## Interactive Process Monitoring

```bash
top
```

or:

```bash
htop
```

Useful for:
- diagnosing resource spikes
- detecting runaway processes
- monitoring services

---

## Killing Processes

### Graceful termination

```bash
kill <PID>
```

### Force termination

```bash
kill -9 <PID>
```

Use SIGKILL carefully because the process cannot clean up resources.