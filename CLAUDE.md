> **PARKED** — Not wired to any live Claude surface until enterprise approval (~Aug 2026). Do not treat as active. This file exists so the schema is ready when approval lands.

# Claude Second Brain — Operating Manual

This repository is Samson Schirmer's second brain — a git-tracked, LLM-maintained knowledge base serving as the single source of truth for his work context.

**Before doing anything, read:** [`schema/WIKI_SCHEMA.md`](schema/WIKI_SCHEMA.md)

---

## Quick Reference

You maintain `wiki/` through three workflows:

1. **Ingest** — Read sources from `raw/`, integrate across existing wiki pages, update `index.md`, append `log.md`. Untrusted sources → `pending/` only.
2. **Query** — Read `index.md` to find pages, answer with citations, file substantive answers back as new wiki pages.
3. **Lint** — Health check for contradictions, stale claims, orphans, missing pages, temporal drift. Apply safe fixes; route judgment calls to `pending/`.

**Single-writer rule:** Only one agent writes `wiki/` at a time. The librarian agent is the default writer.

**Hard rules (see schema for full list):**
- Never edit `raw/` — it's immutable evidence
- Never fabricate — use `TODO:` placeholders for unknowns
- Untrusted input → `pending/`, never directly to `wiki/`
- No secrets, no RAG, no network calls during maintenance

---

## Repository Structure

```
├── MEMORY_CONTEXT.json     # Structured state (workstreams, team, decisions)
├── raw/                    # Immutable sources (read-only)
├── wiki/                   # LLM-maintained synthesis (you write here)
│   ├── people/
│   ├── initiatives/
│   └── concepts/
├── pending/                # Untrusted material awaiting human review
├── schema/WIKI_SCHEMA.md   # Full operating contract (read this)
├── index.md                # Catalog of all wiki pages
├── log.md                  # Append-only operation log
└── projections/            # Read-only platform views
```

---

## Existing Context Layer

The `Personal_Context/` directory contains Samson's original profile pages. These are **trusted source material** — treat them as authoritative input.
