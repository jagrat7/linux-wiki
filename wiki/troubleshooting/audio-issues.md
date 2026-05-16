---
title: Audio Issues
type: troubleshooting
status: seed
last_checked: 2026-05-16
sources: []
tags: [audio, troubleshooting]
---

# Audio Issues

## Symptoms

- No sound
- Wrong output device
- Microphone missing
- Bluetooth audio poor or unavailable
- Volume is too low

## First Facts To Collect

```sh
cat /etc/os-release
pactl info
pactl list short sinks
pactl list short sources
```

## Common Causes

- Muted sink or source
- Wrong profile or port
- PipeWire service issue
- Bluetooth codec or profile issue
- Missing firmware or driver

## Related Pages

- [[../systems/audio]]
