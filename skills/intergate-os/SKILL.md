---
name: intergate-os
description: Collect and organize public source links and key facts for a Linux OS, distro, desktop, or Linux project before adding it to this wiki. Use when Codex needs to extract official docs, manuals, demo videos, install guides, ISO/download links, GitHub/source repos, release notes, community links, screenshots, project ownership, and basic positioning for distro discovery pages.
---

# Intergate OS

## Purpose

Collect the important source links and starter facts for a Linux OS or distro before writing wiki pages.

This skill is for source discovery and extraction, not live system debugging.

## Collect These Links

For each OS or distro, look for:

- Homepage
- Official docs or manual
- Install guide
- Download or ISO page
- Demo video, intro video, tour, or screenshots
- GitHub, GitLab, Codeberg, or other source repo
- Release notes or changelog
- Community links such as Discord, forum, Matrix, Reddit, Mastodon, or mailing list
- Workstation, hardware, or compatibility pages
- Sponsoring organization, parent project, or maintainer page

## Extract These Facts

Keep the first pass concise:

- Name
- Tagline or short positioning
- Base distro or family
- Desktop environment or window manager
- Package manager
- Install method
- Release model or update channel if obvious
- Target users
- Major tradeoffs
- Anything freshness-sensitive, such as latest release or ISO version

## Where To Put It

Before editing, tell the user which pages should receive the information:

- `wiki/distros/<name>.md` for the main distro page
- `wiki/customization/<name>.md` for themes, keybindings, workflow, dotfiles, or desktop behavior
- `wiki/troubleshooting/<name>.md` for project-specific support commands or known failure modes
- `wiki/recipes/<name>-install-template.md` for a generic install checklist
- `wiki/discovery/*.md` for recommendation logic
- `wiki/index.md` for navigation
- `wiki/log.md` for the maintenance entry

Do not create user profile pages.

## Source Preference

Prefer sources in this order:

1. Official homepage
2. Official manual or docs
3. Official source repo
4. Official release notes
5. Official demo video or project media
6. Community pages and reviews

Label community opinion separately from official project facts.

## Output Before Writing

When the user asks to review before adding anything, respond with:

- Links found
- Facts extracted
- Suggested wiki pages
- Open questions or uncertain claims

## Boundaries

- Do not invent missing links
- Do not treat marketing claims as neutral facts
- Do not rely on stale release data without checking current sources
- Do not add broad Linux concepts to a distro page if they belong in `wiki/systems/`
