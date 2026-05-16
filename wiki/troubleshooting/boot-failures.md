---
title: Boot Failures
type: troubleshooting
status: seed
last_checked: 2026-05-16
sources: []
tags: [boot, troubleshooting]
---

# Boot Failures

## Symptoms

- System does not reach login
- System drops to emergency mode
- Bootloader does not show the expected OS
- Graphical login never appears

## First Facts To Collect

```sh
cat /etc/os-release
uname -a
systemctl --failed
journalctl -b -p warning
```

## Common Causes

- Broken bootloader entry
- Kernel or initramfs issue
- Failed filesystem mount
- Graphics driver issue
- Failed display manager

## Related Pages

- [[../systems/boot-and-init]]
- [[graphics-issues]]
