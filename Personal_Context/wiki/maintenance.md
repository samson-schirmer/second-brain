# Maintenance

## Current Setup

- Core profile pages exist in `Personal_Context/`.
- Raw source workflow exists in `Personal_Context/raw/`.
- Wiki synthesis workflow exists in `Personal_Context/wiki/`.
- Agent operating rules exist in root `AGENTS.md`.
- Scheduled maintenance should inspect the repo, ingest any new raw inbox items, run a health check, and push coherent updates to GitHub.

## Health Check Checklist

- `Personal_Context/raw/inbox/` is empty or intentionally waiting.
- `Personal_Context/wiki/index.md` lists all maintained wiki pages, including nested source notes under `Personal_Context/wiki/sources/`.
- `Personal_Context/log.md` has an entry for each ingest or maintenance pass.
- Project statuses in `current-projects` are still current.
- Goals in `goals-and-priorities` reflect the current planning window and have a recent dated source before time-sensitive wording is refreshed.
- Stakeholder dynamics in `team-and-relationships` are still accurate.
- New durable decisions are captured in `decision-log`.
- Open questions are either answered, reworded, or kept intentionally.

## Next Recommended Improvements

- Convert extensionless profile files to `.md` if Samson wants cleaner GitHub and Obsidian rendering.
- Add an Obsidian vault config if this repo becomes the primary reading interface.
- Add templates for source notes, project pages, and weekly reviews.
- Decide whether scheduled jobs should auto-commit every maintenance pass or only when raw inbox items exist.

## [2026-06-01] Maintenance Pass

- Raw inbox: empty (no new sources to ingest).
- Wiki index: no orphan pages detected (all `Personal_Context/wiki/*.md` pages are listed in `Personal_Context/wiki/index.md`).
- Found previously uncommitted ingest work for the 2026-05-22 Writer executive recap email source; syncing it to GitHub as part of this pass.

## [2026-06-03] Maintenance Pass

- Raw inbox: empty (`Personal_Context/raw/inbox/` contains only `.gitkeep`).
- Worktree: clean before edits (`git status --short` returned no tracked or untracked changes).
- Wiki coverage: no orphan wiki pages detected; `Personal_Context/wiki/index.md` still covers the maintained synthesis pages, and the processed source note remains registered.
- Temporal drift risk: several profile pages still use floating time references such as "next 6 months" and "this quarter" without a fresh dated source. No profile text was rewritten during this pass because the repo does not yet contain newer source material to safely re-anchor those claims.

## [2026-06-10] Maintenance Pass

- Raw inbox: empty (`Personal_Context/raw/inbox/` contains only `.gitkeep`).
- Worktree: clean before edits (`git status --short` returned no tracked or untracked changes).
- Wiki coverage: no orphan maintained pages detected across both `Personal_Context/wiki/*.md` and `Personal_Context/wiki/sources/*.md`; `Personal_Context/wiki/index.md` still lists the maintained synthesis pages and the processed source note.
- Maintenance rule tightened: the checklist now explicitly requires recursive coverage for nested source-note pages so future lint passes do not treat top-level coverage as sufficient.

## [2026-06-18] Maintenance Pass

- Raw inbox: empty (`Personal_Context/raw/inbox/` contains only `.gitkeep`).
- Worktree: clean before edits (`git status --short` returned no tracked or untracked changes).
- Wiki coverage: no orphan maintained pages detected across `Personal_Context/wiki/*.md` and `Personal_Context/wiki/sources/*.md`; `Personal_Context/wiki/index.md` still covers the maintained synthesis pages and the processed source note.
- Temporal drift remains concentrated in extensionless profile files and prompts that use floating planning language such as `next 6 months` and `this quarter`, especially in `Personal_Context/current-projects`, `Personal_Context/goals-and-priorities`, and `Personal_Context/wiki/open-questions.md`.
- Checklist wording updated so future maintenance passes require a recent dated source before refreshing time-sensitive goal language.
