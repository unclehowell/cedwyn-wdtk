# cedwyn-wdtk
Cedwyn FOI Requests (/wdtk/) — REPO SPLIT #188

## Data store (7 Nov 2026)
- `public/data/central.json`: this webapp's own store — the central-catalogue fields (id, kind, title, date, status, page) for the record IDs cited in the request files and pages. Derived, read-only, never edited by hand.
- `tools/sync_central.py` fills it from `/api/catalogue/<id>`; `.github/workflows/sync-central.yml` runs it every 6 hours (cron `45 */6 * * *`) and on demand. See #7.
