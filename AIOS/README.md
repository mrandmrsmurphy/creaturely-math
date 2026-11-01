# AIOS: the AI's permanent memory and storage

**Why this folder exists.** Claude Code keeps its memory in `~/.claude/...`, which Murphy's disk-cleaning app can delete. This folder is inside the vault (Google Drive), so it survives. **AIOS is the canonical store.** Anything an AI session would have saved to `~/.claude` goes here instead.

## Protocol

1. **At the start of every session**, after `AGENTS.md`, read `AIOS/MEMORY.md` (the index), then the memory files it points to that bear on the task.
2. **Save memories here**, in `AIOS/memory/`, one fact per file, with the frontmatter below. Add a one-line pointer to `AIOS/MEMORY.md`. Update an existing file rather than duplicating; delete one that proves wrong.
3. **Save session handoffs** in `AIOS/sessions/` (`YYYY-MM-DD <topic>.md`): what was done, what is pending, what to read first. A session that is about to run out of context writes one. The change history of the *math pages* still lives only in `Log/log.md`.
4. **Do not rely on `~/.claude`.** Its memory folder holds only a pointer to this one. Transcripts there (`~/.claude/projects/.../*.jsonl`) are also deletable; anything worth keeping from them is copied here.
5. **Scratch work** (temporary scripts, intermediate output) may use the session scratchpad. It is disposable; never store the only copy of anything there.
6. AIOS holds notes about *how to work with this vault and Murphy*. It does not duplicate vault content (pages, the log, `Sources/`), and it is not a math page: no provenance tags or `[[links]]` into the math are needed, and it is not linked from `Home`.

## The to-do list

**The vault's to-do list is the Agenda in `Meta/Future Directions.md`.** When Murphy asks what needs doing, where the vault stands, or what is open, read the Agenda and answer from it (spot-check it against the pages it points to). Do not rebuild the list from the pages or from memory. Update the Agenda in the same session as any change: move finished items to Settled, add newly found open items under their strand, and log the change in `Log/log.md`. `AIOS/memory/project-vault-state.md` holds only what the Agenda cannot: standing decisions about how to treat the open items.

## Memory file format

```markdown
---
name: <short-kebab-case-slug>
description: <one line, used to decide relevance>
metadata:
  type: user | feedback | project | reference
---

<the fact; for feedback/project add **Why:** and **How to apply:** lines. Link related memories with [[their-name]].>
```

Types: `user` (who Murphy is, preferences), `feedback` (how to work, corrections and confirmed approaches), `project` (ongoing work and constraints not derivable from the vault), `reference` (where things are).
