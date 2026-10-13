# Synergy-Crm
Single-page CSV/Excel-to-dashboard app. No build step, no backend.


# SYNERGY (static build)

Single-page CSV/Excel-to-dashboard app. No build step, no backend.

## Deploy on Netlify
**Drag and drop:** app.netlify.com > Sites > "Deploy manually" > drop this folder (or the zip contents).
**Git:** push these files to a repo, then Add new site > Import from Git. Leave build command empty, publish directory `.`.

## Notes
- Uploaded datasets are stored in each visitor's browser (IndexedDB), not on a server.
- Excel parsing loads SheetJS from cdnjs.cloudflare.com, so the page needs internet access.
- For server-side storage, auth and a database, the next step is the Next.js + Supabase/Postgres version.
