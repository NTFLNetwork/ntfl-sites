# NTFL Network — Supabase Rebuild

This build keeps Supabase as the main source of truth, but it also includes local fallback seed data so the site does not render blank before the database is populated.

## What changed
- Your league logo is used throughout the site.
- Team cards and team pages show ESPN abbreviations and ESPN-style logo URLs.
- Team stats include:
  - Points Per Game For (PPG)
  - Points Per Game Against (PAPG)
  - Points For
  - Points Against
  - Point Differential
- A hidden demo admin login is included in the code but not shown in the UI.
- The commissioner dashboard can seed Supabase from the bundled JSON files.

## Supabase setup
Use the values already wired into `js/config.js`:

- Project URL: `https://zggrwyxtakqpqyrxskiq.supabase.co`
- Publishable key: `sb_publishable_bPPwe-rurJY0mf5bE5RFTw_MPKRNB0_`

## Recommended first step
1. Run `sql/schema.sql` in Supabase.
2. Open `admin.html`.
3. Sign in or use the hidden demo admin path.
4. Click **Seed Supabase** to load the bundled team and schedule data.

## Notes
- Public pages will still show fallback data even when the database is empty.
- The team pages are now dynamic and use `team.html?team=...`.
