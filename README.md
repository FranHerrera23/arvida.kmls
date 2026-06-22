# KMLS — 41 Arvida Proposal

Single-file confidential proposal. The website = `index.html` + `assets/`. Deploy target: Vercel, KMLS subdomain, password-protected.

## Quick start (with Claude Code)
1. Drop the real photos into `assets/` per `ASSET-MANIFEST.md`.
2. Open Claude Code in this folder.
3. Paste the prompt in `START.md` (or below) and follow along.

## The prompt for Claude Code
> Read CLAUDE.md and ASSET-MANIFEST.md. The website is index.html + assets/. First, clean up two leftover test artifacts: run `rm -rf .git assets/neymar/1.jpg`. Then, goal: deploy a static site to Vercel on the subdomain arvida.kmlightingstudio.com, password-protected, from a PRIVATE GitHub repo. Do, in order: (1) help me place + optimize assets (<300KB images, <15MB video); (2) git init + commit + push to a new PRIVATE GitHub repo; (3) deploy to Vercel; (4) add the custom domain and tell me the exact DNS record to create; (5) enable Vercel Password Protection; (6) give me the live URL + password. Pause and ask whenever you need a login or a DNS change. Never commit the PDFs, .docx, screenshots, or old versions — the .gitignore already prevents this; don't loosen it.

## What you need open / ready
- The real project photos, sorted (see ASSET-MANIFEST.md).
- GitHub account (logged in).
- Vercel account (logged in, Pro plan for password protection).
- Access to the DNS settings of your KMLS domain.

## Rules
- Repo PRIVATE. Password protection ON before sharing.
- Only `index.html` + `assets/` get deployed. Everything else stays local.
