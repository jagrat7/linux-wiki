---
name: wiki-navigator
description: Help users enter and use this Linux wiki through the right pages before giving advice. Use when a user asks for Linux recommendations, distro choice, desktop or window-manager choice, gaming/performance/privacy/stability tradeoffs, debugging direction, customization guidance, package-management help, or asks where to start in the wiki. Prefer this skill before answering from memory when the wiki likely has a relevant page.
---

# Wiki Navigator

## Overview

Route the user to the smallest useful set of wiki pages, then answer from those pages plus clearly marked current/source-backed checks when needed.

This skill is for navigation and triage. It does not replace `intergate-os` for ingesting a new distro or `profile` for reading or writing user preference profiles.

## First Pass

1. Read `wiki/index.md`.
2. Open the linked section index that matches the user's intent.
3. Open only the likely leaf pages needed to answer.
4. If a linked page is missing or deleted, say so briefly and route to the nearest existing index.
5. Give the user entry points as wikilinks or local file references, then provide a concise next step.

Use `rg --files wiki` or `rg "<term>" wiki` when the correct page is unclear.

## Route Map

- Distro choice, "what should I pick", gaming, stability, control, beginners: start at `wiki/distros/index.md`, then family pages and distro pages such as `wiki/distros/arch/cachyos.md`, `wiki/distros/fedora/bazzite.md`, `wiki/distros/debian/pop-os.md`, or `wiki/distros/debian/ubuntu.md`.
- Desktop environment or workflow choice: start at `wiki/customization/desktop-environments.md` and `wiki/customization/window-managers.md`, then `wiki/systems/graphics-and-display/index.md`.
- Gaming, GPU, display, Wayland/X11, Steam, Lutris, GameScope, drivers: start at `wiki/systems/graphics-and-display/index.md`.
- Software installation, repositories, update models, Flatpak, distrobox, rpm-ostree, pacman, apt, dnf: start at `wiki/systems/package-management/index.md`.
- Boot, initramfs, bootloaders, startup logs, systemd services: start at `wiki/systems/boot-and-init/index.md`.
- Audio devices, routing, PipeWire, PulseAudio, ALSA: start at `wiki/systems/audio/index.md`.
- Wi-Fi, Bluetooth, DNS, NetworkManager: start at `wiki/systems/networking/index.md`.
- Themes, fonts, icons, terminal, shell, keybindings: start under `wiki/customization/`.
- Repeatable how-to requests: start under `wiki/recipes/` and adapt the appropriate template.

## Discovery Questions

Ask only the questions that change the route or recommendation. Good defaults:

- Optimization target: stability, learning, gaming, control, aesthetics, privacy, speed, hardware support, or low maintenance.
- Hardware: CPU, GPU, laptop/desktop/handheld, unusual Wi-Fi/audio/display hardware.
- Comfort: terminal use, debugging tolerance, willingness to read docs.
- Breakage budget: how much update or driver trouble the user will tolerate.
- Desired role: "teach me Linux" versus "stay out of my way."

If profile-backed personalization is requested or a selected profile may matter, use the `profile` skill before recommending.

## Answer Shape

Keep the answer practical:

- Start with the best entry page or 2-4 page path.
- Then answer the user's immediate question.
- Include tradeoffs when recommending a distro, desktop, package strategy, or customization path.
- Mark gaps: "the wiki has no page for X yet" or "this needs a current official check."
- Use web search only for freshness-sensitive facts, official docs, release/version claims, or missing source-backed details.

## Maintenance Hooks

When the interaction reveals reusable wiki knowledge:

- Suggest adding or updating the relevant wiki page.
- Use `intergate-os` before adding a new OS, distro, desktop, subsystem, official docs page, release notes, install guide, demo video, or source repository.
- Append a concise `wiki/log.md` entry after wiki content changes.
