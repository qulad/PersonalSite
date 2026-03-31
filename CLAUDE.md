# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Personal portfolio site for `qulad.dev`, deployed to **Cloudflare Pages** via zip upload.

The entire site is a **single self-contained `index.html`** — all CSS and JS are embedded inline. No build step, no dependencies, no bundler.

## Deploying

To create a deployable zip:
```bash
zip site.zip index.html cv.pdf
```
Then upload `site.zip` to Cloudflare Pages dashboard → your project → Deployments → Upload assets.

## Structure

- `index.html` — main site (HTML + CSS + JS inline)
- `cv.pdf` — CV file, opens in browser at `/cv.pdf`

## Design system (in `index.html`)

CSS variables are defined in `:root` at the top of the `<style>` block:

| Variable | Purpose |
|---|---|
| `--accent` | Gold accent color (`#c8a96e`) |
| `--text-primary/secondary/tertiary` | Text opacity scale |
| `--bg` | Page background |
| `--border` | Subtle divider lines |
| `--serif` | Cormorant Garamond — headings |
| `--mono` | IBM Plex Mono — body / UI |

## Content to update

Placeholder content lives in these sections of `index.html`:
- **Hero tagline** — "Building things that live on the web." (~line 180)
- **About** — bio paragraphs and skill tags (~line 200)
- **Work** — project names, descriptions, links, and chips (~line 225)
- **Contact** — email address and social links (~line 270)

Social links currently point to `github.com/qulad`, `twitter.com/qulad`, `linkedin.com/in/qulad` — update `href` values to real URLs.
