---
title: Graphics Issues
type: troubleshooting
status: seed
last_checked: 2026-05-16
sources: []
tags: [graphics, troubleshooting]
---

# Graphics Issues

## Symptoms

- Black screen
- Login loop
- Wrong resolution
- External monitor not detected
- Wayland session missing or unstable
- Screen tearing or stutter

## First Facts To Collect

```sh
cat /etc/os-release
uname -a
lspci -k
echo "$XDG_SESSION_TYPE"
```

## Common Causes

- Missing or mismatched GPU driver
- Kernel regression
- Display manager issue
- Wayland compatibility issue
- Hybrid graphics configuration

## Related Pages

- [[../systems/graphics-and-display]]
