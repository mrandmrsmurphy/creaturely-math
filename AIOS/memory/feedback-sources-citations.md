---
name: feedback-sources-citations
description: Dependence on files existing in Sources/ is an AI artifact, not Murphy's convention; saying he wrote it is enough
metadata:
  type: feedback
---

Murphy, 2026-10-10: "The dependence on things being in the Sources folder is not something I started, but an AI artifact. It is enough for me if you say I've written it."

**Why:** the `sources:` fields and `[[SRC ...]]` links were an AI-built apparatus. The provenance information Murphy wants is *whose words these are*, not a path to a file.

**How to apply:** when citing one of Murphy's manuscripts, name it in prose ("Murphy's logic booklet, *From Traditional Logic to Ternary Thought*") and let `provenance:` carry murphy / murphy+ai / ai-synthesis. Do not treat a missing `Sources/` file as an error, do not create SRC stubs, and do not insist he add files. Existing `sources:` links to files that *are* in `Sources/` may stay (they are harmless and useful), but their presence is not required. If a synced file appears later, fine either way.
