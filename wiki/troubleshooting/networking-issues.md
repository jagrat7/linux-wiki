---
title: Networking Issues
type: troubleshooting
status: seed
last_checked: 2026-05-16
sources: []
tags: [networking, troubleshooting]
---

# Networking Issues

## Symptoms

- Wi-Fi adapter missing
- Connected but no internet
- DNS resolution fails
- Bluetooth device does not pair
- Connection works only after reboot

## First Facts To Collect

```sh
cat /etc/os-release
ip link
rfkill list
```

## Common Causes

- Missing firmware
- Disabled radio
- NetworkManager service issue
- DNS configuration issue
- Driver regression

## Related Pages

- [[../systems/networking]]
