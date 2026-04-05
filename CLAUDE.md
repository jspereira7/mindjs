# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

## What This Is

This is an **Obsidian vault** (personal knowledge base) written primarily in Portuguese (Brazil). It is synced to git for backup purposes via the `obsidian-git` plugin. There is no build system, no tests, and no application code.

## Repository Structure

- `00.Notes/` — All user-created notes live here (new file default location)
- `01.Assets/Anexos/` — Attachments and embedded media
- `.obsidian/` — Obsidian configuration (plugins, themes, settings, workspace state)
- `.smart-connections/`, `.smart-env/` — AI plugin embeddings
- `.trash/` — Deleted items

## Git / Backup

Backups are created via the `obsidian-git` plugin. The commit message pattern is:
```
vault backup: <YYYY-MM-DD HH:MM:SS>
```

To create a manual backup, the user triggers the plugin from within Obsidian (command palette: "Obsidian Git: Create backup").

## Key Configuration (`.obsidian/app.json`)

| Setting | Value |
|---|---|
| `vimMode` | `true` |
| `livePreview` | `true` |
| `newFileLocation` | `folder` → `00.Notes` |
| `attachmentFolderPath` | `01.Assets/Anexos` |
| `newLinkFormat` | `shortest` (wikilinks without full paths) |
| `alwaysUpdateLinks` | `true` |
| `promptDelete` | `false` (no confirmation on delete) |

## Active Community Plugins

- **`dataview`** – Query notes dynamically; look for ````dataview` code blocks in notes
- **`templater-obsidian`** – Template system with JS; templates use `<% ... %>` syntax
- **`quickadd`** — Capture macros and automation; configured in `.obsidian/plugins/quickadd/data.json`
- **`obsidian-excalidraw-plugin`** — Embedded `.excalidraw` diagrams
- **`obsidian-git`** — Git commit/push automation
- **`waypoint`** — Auto-generates Maps of Content in `+MOC.md` files
- **`obsidian-custom-frames`** — Embedded web app iframes
- **`todoist-sync-plugin`** — Todoist integration

## Working with Notes

Notes are written in **Obsidian-flavored Markdown**:
- Wikilinks: `[[Note Name]]` or `[[Note Name|display text]]`
- Embeds: `![[Image.png]]` or `![Alt](path)`
- Tags: `#tag` or frontmatter `tags: [tag1, tag2]`
- Callouts: `> [!tip]`, `> [!warning]`, etc.
- Frontmatter (YAML): at the top of notes with `title`, `tags`, `aliases`, `created`, etc.

When creating or modifying notes:
- Place new notes in `00.Notes/`
- Use shortest-form wikilinks (no directory prefix needed)
- Follow the existing frontmatter patterns when present
- Notes are in Portuguese; prefer Portuguese for titles and content unless otherwise specified

## Themes Installed

AnuPpuccin, Cybertron, Dracula for Obsidian, Minimal, Sanctum, Things, Typewriter, Typomagical
