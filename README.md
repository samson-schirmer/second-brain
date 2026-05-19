# Personal Context Portfolio

This repo is Samson Schirmer's Codex-maintained second brain.

It has two jobs:

1. Give AI agents enough context to work with Samson without a long re-introduction.
2. Accumulate knowledge over time as a living, Git-backed wiki.

The setup is inspired by Andrej Karpathy's LLM Wiki pattern: raw sources stay immutable, the wiki is maintained by the LLM, and `AGENTS.md` defines the operating rules.

## Start Here

- `AGENTS.md` — instructions for Codex and other agents maintaining this repo
- `Personal_Context/index` — human-readable index of Samson's current context files
- `Personal_Context/wiki/index.md` — maintained wiki index
- `Personal_Context/log.md` — append-only operating log
- `Personal_Context/raw/` — source material waiting to be processed or preserved

## Daily Workflow

Drop new material into `Personal_Context/raw/inbox/`, then ask Codex:

> Ingest the new second-brain sources and update my personal context portfolio.

Codex should summarize the source, update affected pages, cross-link related ideas, append the log, and commit/push the changes when asked or when running the scheduled maintenance job.

