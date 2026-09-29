# TestDisk

Partition recovery and disk repair tool.

---

## Command Reference

### Syntax
```bash
testdisk [options] [image.dd|/dev/sdX]
```

### Flags
* `/log` — Create a log file.
* `/debug` — Enable detailed logging for debugging purposes.

### Example
```bash
testdisk /log evidence.dd
```