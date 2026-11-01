---
name: reference-locations
description: Where the vault, sources, transcripts and AIOS live, and which locations are vulnerable to deletion
metadata:
  type: reference
---

- Vault root: `/Users/robertmarshallmurphy/Library/CloudStorage/GoogleDrive-<account>/My Drive/My Math` (`<account>` is Murphy's Google Drive login; also mounted as `/Users/robertmarshallmurphy/<account> - Google Drive/My Drive/My Math`). It is a Google Drive folder and a git working tree whose git directory lives outside Drive (see [[reference-git-github]]).
- Instructions: `AGENTS.md` (root), then `Home.md`, then `Meta/Future Directions.md`, then this `AIOS/MEMORY.md`.
- Folders: Foundations, Number, Geometry, Trigonometry, Change, Logic, Symmetry, Measurement, History, Pedagogy, Meta, Sources, Log, images, AIOS.
- Murphy's wider wiki (`raw/murphy/`, `raw/Drafts/`, `wiki/...`) is **outside** this vault; the vault holds only compilations of it in `Sources/`.
- **Vulnerable:** `~/.claude/...` (Murphy's disk-cleaning app can delete it): memory, and session transcripts under `~/.claude/projects/-Users-robertmarshallmurphy-Library-CloudStorage-GoogleDrive-<account>-My-Drive-My-Math/*.jsonl`. The session scratchpad is disposable too. AIOS is the permanent store ([[feedback-faithful-recording]] and the others live here for that reason).
- Checks used on edits: PyYAML validation of every page's frontmatter outside `Sources/`; a link check against page names.
