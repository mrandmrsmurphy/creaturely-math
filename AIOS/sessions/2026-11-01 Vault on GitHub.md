# 2026-11-01: the vault goes on GitHub

Protocol: `AGENTS.md`; read `Home.md`, `Meta/Future Directions.md` (the Agenda), `AIOS/MEMORY.md`. Changes are in `Log/log.md` under 2026-11-01.

## Done
1. Vault put under git with the git directory outside Google Drive (`~/.gitdirs/creaturely-math`); `.git` in the vault is a pointer file. See `AIOS/memory/reference-git-github`.
2. Public repo: `mrandmrsmurphy/creaturely-math`, one commit (history squashed; the first repo was deleted and recreated so earlier commits no longer exist anywhere). CC BY 4.0 including `Sources/`.
3. Four third-party PDFs removed from `images/` and replaced by links in `Meta/Reading List` (two new entries).
4. The school's name removed from the vault ("a good school" or neutral wording; wiki page names end `-at-a-good-school`); the work e-mail removed from `AIOS/memory/reference-locations` (paths use `<account>`). Murphy's rule: never put either back.
5. "Board" renamed "the Agenda" everywhere (Murphy never chose "Board" and dislikes it). Agenda item 9 (go-public decisions) closed.
6. Obsidian Git auto-commits and pushes; `.obsidian/plugins/` is ignored.

## Watch
- The commit author is Murphy's personal gmail, now public. He did not say whether to change it to a GitHub `noreply` address.
- If Obsidian Git reports "unrelated histories", the GitHub `origin/main` is the right history; do not merge.
- The original PDFs are in `~/.claude-tmp/pdf-backup/` (disposable); the Taylor & Francis DOI link returned 403 to a script (likely bot-blocking), not checked in a browser.
- `gh` does not work from inside the vault (pointer `.git`); use plain `git`, and `gh` only with `owner/repo`.
