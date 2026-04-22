# NEVBC Leaderboard

Public web dashboard of season stats for **Northeast Volleyball Club**,
built from Hudl exports.

**Live:** https://scgrandpre.github.io/nevbc-leaderboard/

## Data & privacy

Stats are pulled from Hudl with club permission. The dashboard displays:

- Full first + last names of rostered players (youth athletes)
- Season-to-date aggregated stats (kills, digs, aces, attack %, etc.)

No contact info, birthdates, or addresses. If a parent or player wants
their name removed or displayed as first-name-only, reach out and we'll
redeploy within the day.

## What's here

- `index.html` — root page served by GitHub Pages
- `NEVBC_Leaderboard_broadcast.html` — same content, addressable directly

## Rebuilding

This file is built elsewhere (see the BUVC project's `RUNBOOK.md`) and
dropped in. To refresh:

```bash
# from the Hudl/ dev folder
python3 hudl_stats_exporter.py                      # pick NEVBC
python3 Hudl_exports_bundle/build_leaderboard.py    # pick NEVBC

# copy the built file here
cp ~/Documents/Claude/Hudl/NEVBC_Leaderboard_broadcast.html index.html
cp ~/Documents/Claude/Hudl/NEVBC_Leaderboard_broadcast.html NEVBC_Leaderboard_broadcast.html
git add -A && git commit -m "Refresh" && git push
```
