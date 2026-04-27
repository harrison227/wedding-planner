# Wedding Table Planner

Interactive seating chart for Harrison & Gabby's wedding.

## Features

- 130 guests pre-loaded, split across 14 tables (1 bridal + 13 round)
- Side colour-coding (Gabby's pink, Harrison's blue) with group labels
- Bridal table as a head-table rectangle, with bride and groom centred
- Round tables in a draggable floor plan — grab the handle on any table to reposition
- Drag any guest between tables, onto a specific seat, or onto another guest to swap
- Couples are linked — drag one and their partner follows automatically
- Pair/unpair via the guest edit modal (double-click any guest)
- Smart shuffle keeps each side together (no Gabby family at a Harrison-friends table)
- Bulk import, JSON/CSV export, print-friendly layout
- **Live cloud sync** via Firebase Realtime Database — share the URL and edits propagate in real time

## Live sync setup

1. Create a [Firebase project](https://console.firebase.google.com)
2. Build → Realtime Database → Create (start in **test mode**)
3. Project settings → Your apps → Web app → copy the config object
4. In the planner: ⋮ menu → Settings → paste the config in **Live sync (Firebase)** → Save
5. Page reloads with live sync enabled. Both you and your partner load the same URL — every change syncs.

Without sync configured, the planner uses browser localStorage (each browser has its own copy).

## Hosting

Static HTML — works on any host. GitHub Pages, Render, Netlify, Vercel, Cloudflare Pages all work out of the box.
