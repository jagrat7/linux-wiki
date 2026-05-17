---
name: update-os
description: Update freshness-sensitive wiki information for an existing Linux OS, distro, desktop, or Linux project after a new release, renamed/replaced component, changed install path, updated ISO/download, or changed upstream guidance. Use when the user asks to refresh current OS facts such as latest version, release notes, changelog, install media, supported base distro, included desktop/window-manager components, component replacements, upgrade steps, screenshots/media, project links, or status changes. Prefer official sources and append wiki maintenance logs.
---

# Update OS

## Purpose

Refresh existing wiki pages when a Linux OS, distro, desktop, or related project changes after initial ingest.

Use this for update passes like "Omarchy 4.0 released; update relevant info", "Omarchy replaced Waybar with Quickshell", or "refresh CachyOS latest ISO and package guidance."

## Required Input

Start from one of:

- An existing wiki page or OS/project name already present in `wiki/`
- An official homepage, release page, changelog, source repository, docs page, or download page
- A user-provided release/version claim that needs verification

If neither a project name nor canonical source is clear, ask for the OS/project name or official source before editing.

## Current Source Check

For freshness-sensitive claims, verify current information before writing. Prefer sources in this order:

1. Official release notes, changelog, or tagged source release
2. Official docs/manual
3. Official download or ISO page
4. Official homepage
5. Official source repository metadata
6. Community reports, only for observed issues or reputation, labeled as community-sourced

Check dates and version numbers explicitly. Do not preserve stale "latest" claims without confirming them.

## Update Scope

Search the wiki for the OS/project name, previous version, old component name, and new component name before editing:

- Main distro or system page under `wiki/distros/` or `wiki/systems/`
- Related customization, troubleshooting, recipe, and discovery pages
- `wiki/index.md` if page titles, links, categories, or navigation changed
- Existing system/component pages that may need new links, deprecation notes, or index updates
- `wiki/log.md` for the maintenance entry

Only update pages affected by the verified change. Do not rewrite unrelated guidance.

## What To Refresh

Consider whether the release changes:

- Latest release/version, release date, ISO/download links, or supported upgrade path
- Base distro, kernel, desktop environment, window manager, compositor, shell, launcher, bar, terminal, editor, package manager, installer, or default apps
- Installation, upgrade, rollback, rescue, backup, or migration instructions
- Hardware support, GPU/display/session guidance, boot requirements, secure boot, filesystem, or snapshots
- Screenshots, demo videos, docs, community links, support channels, or project ownership
- Known issues, breaking changes, deprecations, renamed commands, or changed config paths
- Recommendation tradeoffs in discovery pages

## Component Replacements

When an update replaces one component with another, verify and update the full relationship instead of swapping a single word:

- Confirm the old component, new component, and effective version/date from official sources when possible.
- Update component lists, prose, source URLs, wikilinks, tags, and `last_checked` on every affected page.
- Add a seed page under `wiki/systems/` for the new component if it is important beyond one distro.
- Keep the old component page if it remains generally useful, but remove or qualify claims that the OS/project still uses it.
- Search for spelling variants and common forms, such as `Quick Shell`, `Quickshell`, `quick-shell`, and mistaken user spellings.
- Note uncertainty clearly if the source proves that a component is present but not whether it fully replaces the old one.

## Raw Sources

If preserving source material, store immutable captures under `raw/` using a clear project/date/source naming pattern. Do not overwrite older raw files.

Wiki pages may synthesize sources, but source URLs and `last_checked` must reflect the new verification date.

## Editing Rules

- Preserve existing page structure and frontmatter where possible.
- Update `last_checked` on pages whose facts were re-verified.
- Keep `sources` current and remove dead or superseded links only when replacements are verified.
- Separate official facts from recommendations and community reports.
- Use wikilinks for related pages where useful.
- Keep commands in fenced code blocks or inline code.
- Avoid broad concept explanations that belong in shared `wiki/systems/` pages.

## Log Entry

After edits, append one concise entry to `wiki/log.md`:

```md
## [YYYY-MM-DD] update-os | Refreshed <project> for <version/change> using official <sources>
```

## Output Shape

When the user asks for a dry run or review, do not edit. Return:

- Verified changes
- Sources checked
- Pages that should change
- Uncertain claims or follow-up checks

When editing, finish with:

- Pages changed
- Current version/date facts confirmed
- Sources used
- Any claims left uncertain
