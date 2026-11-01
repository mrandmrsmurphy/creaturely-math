---
name: reference-git-github
description: How the vault is under git and on GitHub: repo name, git dir outside Drive, privacy, licence, commit rule
metadata:
  type: reference
---

- Repo: `mrandmrsmurphy/creaturely-math` on GitHub, made public on Murphy's go-ahead (see the log, 2026-11-01). Licence CC BY 4.0 (`LICENSE`), including `Sources/` (Murphy wrote them and wants them used); `third-party` material is excluded (see `README.md`). The history was squashed to one commit before going public. **Never put the school's name or Murphy's work e-mail in the vault** (Murphy's rule): use "a good school" and `<account>`. Third-party papers are linked in `Meta/Reading List`, not stored.
- The git directory is **outside Google Drive**: `~/.gitdirs/creaturely-math`. The vault's `.git` is only a one-line pointer file. Reason: Drive syncing a `.git` directory corrupts it. Never run `git init` again or move `.git` into the vault. If `~/.gitdirs` is lost, the GitHub remote is the backup: clone it elsewhere and re-point.
- `.gitignore` excludes `.DS_Store`, `.obsidian/workspace*.json`, `.trash/` and Drive conflict copies. The rest of `.obsidian/` is tracked.
- **Obsidian auto-commits and auto-pushes (Murphy, 2026-11-01), so a session need not ask before committing or pushing and should not worry about it.** When a session commits itself, end messages with the Co-Authored-By line the session gives. Record vault changes in `Log/log.md` as usual; the git history is not a substitute and pages still carry no version notes.
- Quirks: `gh` does not recognise the `.git` pointer file, so `gh repo create --source=.` and other `gh` commands that need a local repo fail; use plain `git` for local work and `gh` only with an explicit `owner/repo`. The remote is `origin` (HTTPS). Pushes over HTTPS failed with HTTP 400 until `http.postBuffer` was raised (set to 150 MB in this repo's config, which lives in the external git dir).
- Related: [[reference-locations]].
