# SchoolLedger MVP

School Finance & Billing system — built by **Providers Consultancy** (Ecow).
A re-skin of the Bamobi FieldBar POS into a Student Billing / Debt-Collection +
Digital Receipts PWA.

## What it does
- **Admin**: add students (with opening fee from a template), manage fee
  templates, view the owner dashboard (Total Expected / Collected / Outstanding /
  Defaulters), set role PINs.
- **Collector**: search a student by name / ID / class, record a partial or full
  payment, instantly reduce their balance, and generate a receipt.
- **Teacher**: read-only dashboard + student balances.
- **Digital receipts**: tap "Send WhatsApp" → opens a pre-filled `wa.me` message
  to the guardian (free, no API). Print fallback included.
- **Offline-first**: all data lives in the device's `localStorage`. Works with no
  internet. (Phase 2: optional Firestore cloud sync + auto-send receipts.)

## Stack
Pure static PWA — HTML/CSS/JS, `localStorage`, GitHub Pages. No server required.
No build step. Matches the FieldBar POS architecture (roles + PIN auth, offline-first).

## Deploy (GitHub Pages)
1. Create repo `SchoolLedger` under `ekowsameb-cell`.
2. Push these files to the default branch:
   - `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md`
3. Repo → Settings → Pages → Source: deploy from branch (root).
4. Live at `https://ekowsameb-cell.github.io/SchoolLedger/`

## Phase 2 (planned, not built)
- Firestore backend (flip the storage module — screens don't change).
- Cloud Function auto-sends WhatsApp/SMS receipt on payment.
- Live multi-device sync (also retrofittable to Bamobi FieldBar POS).

## Default PINs
All roles default to `0000`. Change in Admin → Settings before any real use.

---
⚡ Powered by Providers Consultancy
