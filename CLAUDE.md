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

## ⚠️ Asset prep (do as part of task 1)
The photo folders already have material, but it's messy. For each project folder under `assets/`:
- **Photos are often nested inside a SUBFOLDER** (e.g. `collector/Assets_penthouse_artcollector/`, `pezet3/Pezet3_ramsa copy/`, `jet/Assets_privateplane/`, `yacht/Assets_yatch/`, `kathy/Assets_penthouselima/`, `mariana/_Assets_penthouselima_2/`). **Flatten them**: move the images up so they sit directly in the project folder, then delete the empty subfolder.
- Filenames are **random** (WhatsApp…, Proyecto Garcia…, A12063…, DSC_…). Rename/select to sequential `1.jpg … N.jpg` where **N matches `photos:N`** in the `PROJECTS` object in `index.html` (the manifest lists every N). `1.jpg` is the cover. If a folder has more photos than N, keep the best N (or raise `photos:N`).
- Rename Karen's photo (random name in `assets/studio/`) to `assets/studio/karen.jpg`.
- **Rename two folders** (client names → generic): `assets/kathy/` → `assets/residence-1/`, and `assets/mariana/` → `assets/residence-2/`. ⚠️ These are NOT empty — they hold ~11 and ~5 photos inside subfolders; move + rename those too.
- Optimize everything: JPG ~1600–2000px, <300KB each; video <15MB.
- Empty folders still to be filled by the client: gustavo, fisher, golden, palmbeach, vivagym, saadiyat (saadiyat has 5 photos but needs the video.mp4). Leave their numbered slots; `onerror` hides anything missing.

## ⚠️ v6 audit already applied to index.html (do NOT redo)
The HTML already contains the full v6 edit (validated): Invitation shortened, Approach+Cinema merged into one "A Shared Language" section, Material First shortened, Arrival folded into the Plaster card, Scope of Work rebuilt as **3 zigzag stage sections** (not cards) each with a 3-photo strip, a new **Coordination** section, Room by Room compacted, Investment = **$35,000**, closing line cleaned, eyebrows renumbered 01–11. Your job is assets + deploy, not content.

### New / changed assets from v6
- **NEW folder `assets/scope/`** needs 9 images: `stage1-1.jpg stage1-2.jpg stage1-3.jpg · stage2-1..3 · stage3-1..3` (RCP/plan, concept render, fixture schedule; coordination/site/drawings; aiming/final scene/walkthrough). Placeholders show until added — fine to deploy without them.
- No longer used: `assets/arvida/cinema.jpg`, `assets/arvida/stair.jpg` (those sections were removed).
- Visible `to confirm` chips mark specs Karen must validate (control system, file formats, photometric stage) — leave them until Karen confirms.

## Tasks (do in this order)
1. Do the asset prep above (rename to 1.jpg…N.jpg, rename Karen's photo, rename the 2 folders, optimize). Photos live inside SUBFOLDERS — flatten them first.
2. `git init`, commit, push to a **NEW PRIVATE** GitHub repo.
3. Deploy to **Vercel** (import the repo).
4. Add custom domain `arvida.kmlightingstudio.com`; print the **exact DNS record** I need to create at my registrar.
5. Enable **Vercel Password Protection**.
6. Give me the live URL + the password.

Stop and ask me whenever you need a login (GitHub / Vercel) or the DNS change — don't guess.
