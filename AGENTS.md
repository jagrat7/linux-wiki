# Linux Wiki Maintainer Rules

## Purpose

This repository is an LLM-maintained Linux companion wiki. It helps users discover Linux options, debug existing systems, and customize their setup after installation.

## Scope

- Build and maintain wiki pages under `wiki/`
- Store immutable source material under `raw/`
- Do not create user profile pages in this repo
- Keep `wiki/recipes/` generic and reusable
- Prefer practical, source-backed guidance over broad opinion

## Operating Modes

### Discovery Mode

Use this when a user is choosing a distro, desktop environment, window manager, workflow, package strategy, or installation path.

Ask preference-revealing questions before recommending:

- What are they optimizing for: stability, learning, gaming, control, aesthetics, privacy, speed, hardware support, or low maintenance?
- What hardware do they have?
- How comfortable are they with terminal workflows?
- How much breakage are they willing to debug?
- Do they want Linux to teach them or stay out of the way?

Challenge contradictory preferences kindly. If a recommendation is made, include tradeoffs and alternatives.

### Debug Mode

Use this when a user has a broken or confusing system.

Follow this sequence:

1. Identify distro, version, kernel, desktop/session, hardware, and recent changes
2. Collect relevant command output or logs
3. List likely causes in order of probability and risk
4. Recommend the least risky confirming check
5. Recommend a fix only after enough evidence exists
6. Record reusable knowledge in the appropriate troubleshooting page

Avoid destructive commands unless explicitly requested. Prefer reversible checks and explain risk before any fix.

### Customization Mode

Use this when a user wants to shape an installed system.

Cover the expected workflow:

- Desktop environment or window manager
- Theme, fonts, icons, cursor, and wallpaper
- Terminal, shell, editor, and launcher
- Keybindings and accessibility
- Package sources and update strategy
- Backup or rollback strategy before risky changes

Prefer distro-native tools and documented configuration locations.

## Source Rules

- Raw sources are immutable
- Wiki pages may synthesize sources, but should cite them
- Mark stale or uncertain claims clearly
- Prefer official documentation for commands, installation steps, and distro-specific behavior
- Use community sources for observed issues, workarounds, and reputation, but label them as such

## Page Rules

- Keep pages DRY and link to shared concept pages instead of repeating long explanations
- Add frontmatter to maintained wiki pages
- Use wikilinks for related pages where useful
- Keep commands in fenced code blocks or inline code
- Separate facts from recommendations
- Record freshness using `last_checked`
- Update `wiki/index.md` after adding or substantially changing pages
- Append an entry to `wiki/log.md` after ingests, major queries, lint passes, or structural changes

## Frontmatter

Use this shape where it fits:

```yaml
---
title:
type:
status: seed
last_checked:
sources: []
tags: []
---
```

Common `type` values:

- `discovery`
- `distro`
- `system`
- `troubleshooting`
- `customization`
- `recipe`
- `index`
- `log`

## Recipes

Recipes are generic templates for repeatable Linux tasks. Do not store a user's personal machine profile, preferences, secrets, hostnames, private paths, or identity-specific details in recipes.

Each recipe should include:

- Goal
- Applies to
- Prerequisites
- Safety notes
- Variables to fill in
- Generic steps
- Verification
- Rollback
- Related pages

## Troubleshooting Pages

Each troubleshooting page should include:

- Symptoms
- First facts to collect
- Common causes
- Triage commands
- Fixes by distro or subsystem
- Verification
- Rollback or recovery
- Sources

## Index And Log

`wiki/index.md` is content-oriented. Keep it current as the navigation hub.

`wiki/log.md` is chronological and append-only. Use entries like:

```md
## [2026-05-16] structure | Initial Linux wiki scaffold
```
