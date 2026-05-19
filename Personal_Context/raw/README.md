# Raw Sources

This folder is the source layer of the second brain.

Raw sources are the materials Codex reads from but does not casually rewrite. They can include meeting notes, articles, exported chats, transcripts, PDFs, project notes, screenshots, and personal reflections.

## Folders

- `inbox/` — drop new items here when they need to be processed.
- `assets/` — images and attachments referenced by raw notes.
- `processed/` — optional holding area for sources after they have been ingested.

## Source Rules

- Keep source filenames descriptive.
- Prefer Markdown or plain text when possible.
- Preserve original wording when the source itself matters.
- If a source contains sensitive material, label it clearly at the top before ingestion.
- After Codex ingests a source, it should create or update synthesis pages in `../wiki/` and append `../log.md`.

