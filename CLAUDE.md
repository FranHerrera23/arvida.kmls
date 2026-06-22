# KMLS — 41 Arvida Proposal · Build & Deploy

## What this is
A single-file, confidential lighting-design proposal for **Karen Mannheim Lighting Studio (KMLS)**, project **"41 Arvida"** (Coral Gables), in partnership with **Studio Valle de Valle**. The whole site is ONE static file (`index.html`) plus an `assets/` folder of images and one video. No build step, no framework, no dependencies.

## The goal
Deploy as a **static site on Vercel**, on a KMLS subdomain (e.g. `arvida.kmlightingstudio.com`), **PASSWORD-PROTECTED**. One shareable link. No zip. Nothing that can break.

## ⚠️ Confidential — read first
This deck names private clients and fees. Therefore:
- The GitHub repo MUST be **PRIVATE**.
- Enable **Vercel Password Protection** (Deployment Protection) before sharing the URL.
- NEVER commit the source PDFs, .docx, screenshots, or the old HTML versions. The included `.gitignore` already restricts the repo to `index.html` + `assets/` (+ these .md files) only. **Do not loosen it.**

## Files in this repo
- `index.html` — the proposal. Do NOT rename (Vercel serves `index.html` at the root).
- `assets/` — image/video folders (already scaffolded, currently empty).
- `ASSET-MANIFEST.md` — exact map of where every photo / render / video goes.

## Asset rules
- **Project photos:** `assets/<project>/1.jpg … N.jpg` (`1.jpg` = cover). Counts per project are in `ASSET-MANIFEST.md` and in the `PROJECTS` object inside `index.html` (`photos:N`).
- **Arvida renders:** `assets/arvida/…` → `hero, approach, cinema, material, mood, plaster, wood, microcement, felt` (`.jpg`).
- **Karen:** `assets/studio/karen.jpg`. ⚠️ There is NO team section — only Karen. There is no `assets/team/`.
- **Saadiyat video:** `assets/saadiyat/video.mp4` (shows as the first slide of that gallery).
- **Optimize:** JPG ~1600–2000px long edge, quality ~80, **<300KB each**. Video: MP4 H.264 1080p, **<15MB**.
- Missing images are auto-hidden by `onerror` in the HTML — nothing breaks if one is absent.

## Tasks (do in this order)
1. Help place + optimize the assets per `ASSET-MANIFEST.md`.
2. `git init`, commit, push to a **NEW PRIVATE** GitHub repo.
3. Deploy to **Vercel** (import the repo).
4. Add custom domain `arvida.kmlightingstudio.com`; print the **exact DNS record** I need to create at my registrar.
5. Enable **Vercel Password Protection**.
6. Give me the live URL + the password.

Stop and ask me whenever you need a login (GitHub / Vercel) or the DNS change — don't guess.
