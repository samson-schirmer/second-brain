# Maintenance

## Current Setup

- Core profile pages exist in `Personal_Context/`.
- Raw source workflow exists in `Personal_Context/raw/`.
- Wiki synthesis workflow exists in `Personal_Context/wiki/`.
- Agent operating rules exist in root `AGENTS.md`.
- Scheduled maintenance should inspect the repo, ingest any new raw inbox items, run a health check, and push coherent updates to GitHub.

## Health Check Checklist

- `Personal_Context/raw/inbox/` is empty or intentionally waiting.
- `Personal_Context/wiki/index.md` lists all wiki pages.
- `Personal_Context/log.md` has an entry for each ingest or maintenance pass.
- Project statuses in `current-projects` are still current.
- Goals in `goals-and-priorities` reflect the current quarter.
- Stakeholder dynamics in `team-and-relationships` are still accurate.
- New durable decisions are captured in `decision-log`.
- Open questions are either answered, reworded, or kept intentionally.

## Next Recommended Improvements

- Convert extensionless profile files to `.md` if Samson wants cleaner GitHub and Obsidian rendering.
- Add an Obsidian vault config if this repo becomes the primary reading interface.
- Add templates for source notes, project pages, and weekly reviews.
- Decide whether scheduled jobs should auto-commit every maintenance pass or only when raw inbox items exist.

