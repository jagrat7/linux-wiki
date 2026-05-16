---
title: Package Conflicts
type: troubleshooting
status: seed
last_checked: 2026-05-16
sources: []
tags: [packages, troubleshooting]
---

# Package Conflicts

## Symptoms

- Upgrade fails
- Package manager reports dependency conflicts
- Application cannot be installed
- System has mixed package sources

## First Facts To Collect

```sh
cat /etc/os-release
```

Record the exact package-manager command and full error output.

## Common Causes

- Partial upgrade
- Mixed repositories
- Held packages
- Conflicting third-party package
- Outdated package database

## Related Pages

- [[../systems/package-management]]
- [[../recipes/install-software-template]]
