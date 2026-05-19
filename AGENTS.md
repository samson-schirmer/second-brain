# Codex Second Brain Operating Manual

This repository is Samson Schirmer's personal context portfolio and second brain. Treat it as a living knowledge base, not a static profile.

## Core Model

Use the LLM-wiki pattern:

- `Personal_Context/raw/` contains source material. Sources are read-only unless Samson explicitly asks to edit or remove them.
- `Personal_Context/wiki/` contains LLM-maintained synthesis pages. Codex may create and update these pages.
- `Personal_Context/log.md` is append-only. Every ingest, maintenance pass, major query, or structural change gets a dated entry.
- `Personal_Context/index` is the high-level map of the personal context portfolio.
- Root `README.md` explains the repo for humans.

## Maintenance Principles

- Preserve Samson's voice: direct, specific, action-oriented, no consultant-speak.
- Prefer concrete facts, dates, people, systems, and projects over vague summaries.
- Do not invent personal facts. If something is inferred, label it as an inference.
- Keep raw sources separate from synthesized wiki pages.
- When new information contradicts older information, do not silently overwrite. Update the relevant page and note the tension in `Personal_Context/wiki/open-questions.md`.
- Maintain cross-links using relative Markdown links.
- Keep pages useful to future AI agents: short enough to scan, specific enough to act.
- Use Git intentionally. Commit related updates together with clear messages.

## Ingest Workflow

When Samson asks to ingest new context, or when a scheduled maintenance job runs:

1. Inspect `Personal_Context/raw/inbox/` and any source paths Samson named.
2. Read the relevant source material.
3. Create or update a source note in `Personal_Context/wiki/sources/`.
4. Update affected context pages, especially:
   - `identity`
   - `role-and-responsibilities`
   - `current-projects`
   - `team-and-relationships`
   - `tools-and-systems`
   - `communication-style`
   - `goals-and-priorities`
   - `preferences-and-constraints`
   - `domain-knowledge`
   - `decision-log`
5. Update `Personal_Context/wiki/index.md`.
6. Append `Personal_Context/log.md`.
7. Run a quick consistency check with `rg` and `git diff`.
8. Commit and push only if the changes are coherent and no unrelated user edits would be overwritten.

## Query Workflow

When answering questions from this repo:

1. Read `Personal_Context/index` and `Personal_Context/wiki/index.md` first.
2. Search with `rg` for specific names, projects, tools, or concepts.
3. Answer with citations to the files used.
4. If the answer creates durable synthesis, offer to file it into the wiki.

## Lint Workflow

During maintenance, look for:

- stale project statuses
- missing cross-links
- orphan wiki pages
- contradictions between profile pages
- uncaptured decisions
- sources in `raw/inbox/` that have not been processed
- useful questions Samson should answer next

Record findings in `Personal_Context/wiki/open-questions.md` or `Personal_Context/wiki/maintenance.md`.

## GitHub Sync

This repo is connected to `origin`. The intended steady state is:

- local Markdown stays readable in Codex and Obsidian
- GitHub stays current as the durable backup and portable context source
- scheduled maintenance commits small coherent updates rather than large noisy rewrites

