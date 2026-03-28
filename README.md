# OpenAI Codex Docs Mirror

Local mirror for official OpenAI Markdown docs, focused on Codex and API docs.

## Open-Source Positioning

This repository is an open mirror of publicly available OpenAI documentation, designed to make
agent-oriented document ingestion and retrieval easier.

- Canonical source remains the official OpenAI docs site.
- This mirror does not redefine or replace official documentation.
- We only mirror documentation discovered from official `llms.txt` indexes.
- Each mirrored file keeps source metadata (`url`, `sha256`, `fetched_at`) in `docs/docs_manifest.json`.

This repository is designed for automation-first ingestion:
- Periodically fetches `llms.txt` indexes from OpenAI docs
- Resolves all linked `.md` pages
- Stores mirrored files under `docs/`
- Writes `docs/docs_manifest.json` with hashes and source metadata

## Sources

Configured in `config/sources.json`:
- `https://developers.openai.com/codex/llms.txt`
- `https://developers.openai.com/api/docs/llms.txt`

## Layout

- `scripts/fetch_openai_docs.py`: fetcher + manifest generator
- `config/sources.json`: source definitions
- `docs/`: mirrored markdown content and manifest
- `.cnb.yml`: CNB scheduled + manual sync workflow
- `.cnb/web_trigger.yml`: CNB page button configuration

## Run locally

```bash
pip install -r scripts/requirements.txt
python3 scripts/fetch_openai_docs.py
```

Optional strict mode:

```bash
STRICT_FETCH=1 python3 scripts/fetch_openai_docs.py
```

## Automation

This repository supports both CNB and GitHub Actions automation:

- CNB scheduled sync daily: `main -> "crontab: 0 0 * * *"`
- CNB manual sync button on `main` branch page: **Sync OpenAI Docs**
- GitHub Actions scheduled sync daily: `.github/workflows/update-docs.yml`
- Push / PR validation on `main` for fetcher changes (`scripts/**`, `config/**`, `.cnb.yml`, `.cnb/web_trigger.yml`)

## Notes

- Source content remains property of OpenAI.
- This repository stores mirrored copies to support machine-readable indexing and agent retrieval workflows.
- Official docs should always be treated as the source of truth when discrepancies appear.

## Roadmap

1. Keep a stable daily sync baseline.
2. Preserve manual sync triggers for urgent refreshes.
3. Add retrieval-focused artifacts (diff summaries / normalized indexes) to improve agent read quality.
4. Keep CNB and GitHub Actions workflows aligned with the same daily sync policy.
