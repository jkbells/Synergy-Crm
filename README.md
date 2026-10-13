# SYNERGY CRM — backend scaffold
Stack: Next.js (App Router) · Prisma · Postgres (Neon or Supabase) · Supabase Auth + Storage · Netlify.
## Setup
1. `cp .env.example .env.local` and fill values. 2. Create a private Supabase Storage bucket named `datasets`.
3. `npm i && npx prisma migrate dev --name init` (production: `npm run migrate`). 4. `npm run dev`.
## Deploy (Netlify)
Connect the repo; netlify.toml is preconfigured. Add every variable from .env.example in Site settings → Environment. Service-role key stays server-side only.
## Security model
Each route calls `requireWorkspace()`; every query filters by `workspaceId`. Inputs validated with zod. Add rate limiting (e.g. Upstash) before launch.
## Status
Done: schema (contacts, companies, deals/pipelines, activities, tasks, datasets), auth helper, contacts/deals/import routes.
TODO: companies, activities, tasks, datasets upload+analyze routes (port the analytics engine from synergy.html), frontend, email sync, workflows.



https://synergy-it-crm.netlify.app/


<img width="1915" height="977" alt="Screenshot 2026-10-13 121049" src="https://github.com/user-attachments/assets/4a14225b-83be-4705-87cb-c5a13c3b45c7" />
