# Pherni Coming-Soon

**Document:** `CLAUDE.md`
**Version:** 1.0.0
**Status:** Project Soliton
**Date:** June 2026

---

## 1. Identity

| Field | Value |
|-------|-------|
| Project | Pherni Coming-Soon |
| Type | Web — static landing page (coming-soon) |
| Started | 2026-06-13 |
| Status | Active |

Forked to `-b` per the standing parallel-fork rule ([[feedback_parallel_project_fork]]): a `pherni`
folder already existed (a parallel session); it is left untouched and unread.

## 2. Purpose

Ship a live coming-soon page for **pherni.com** that mirrors the St. Agni homepage exactly, branded
PHERNI, hosted free on GitHub Pages. The loop closes when `https://pherni.com` serves the page over
HTTPS.

## 3. Core (∂_0)

A faithful St. Agni homepage clone — fixed white header (SHOP / centered wordmark / SEARCH (0)),
full-bleed hero, centered hero caption, white footer — with three swaps: PHERNI logo, `banner.png`
hero, and `Coming Soon` in place of `Fall Winter 26`.

## 4. Gradient (∇τ)

Pixel-faithful to the reference; minimal, fast (no webfonts/JS framework), self-contained. "Good" =
indistinguishable in structure from St. Agni, on-brand for Pherni, instant to load.

## 5. Shells

| Shell | Content |
|-------|---------|
| S₁ Canonical | The St. Agni homepage layout (header + full-bleed hero + scroll-revealed footer) |
| S₂ Typical | Minimal fashion-house landing pages |
| S₃ Peripheral | Generic "coming soon" splash pages (rejected — too far from the reference) |

## 6. Boundary (∂χ)

Excluded: working shop/search/cart, live footer links, analytics, cookie/consent banner, the
third-party chat bubble. Footer minimized to Pherni-relevant items (Founder decision). Header chrome
kept faithful but non-functional.

## 7. References (External Trace)

- Reference site: `https://int.st-agni.com/`
- Inputs (transient, in `~/Downloads/`): `banner.png` (4409×2400), `LOGO.png` (white PHERNI wordmark)
- Master archived: `_src/banner-original.png`

## 8. Stacks Loaded

None (outside the film pipeline — a plain web build).

## 9. Vocabulary (Project-Specific)

| Term | Definition |
|------|------------|
| Hero | The full-viewport banner section with the centered caption |
| Caption | The `Coming Soon` line (replaces St. Agni's `Fall Winter 26`) |

## 10. File Map

| Path | Content |
|------|---------|
| `index.html` | The page (inline CSS) |
| `assets/banner.jpg`, `assets/banner-mobile.jpg` | Hero, srcset-swapped |
| `assets/logo-black.png`, `assets/logo.png` | Wordmark (black for header / white original) |
| `_src/banner-original.png` | 15 MB master (git-ignored, not deployed) |
| `.nojekyll` | GitHub Pages: serve assets untouched |
| `CNAME` | Phase 2 — `pherni.com` |
| `README.md` | Deploy + DNS notes |

## 11. Decision Log

| Date | Decision | Reasoning |
|------|----------|-----------|
| 2026-06-13 | Footer minimized to Pherni-relevant (newsletter + Instagram/Contact/Privacy) | Founder choice; St. Agni's boutiques/stockists/loyalty labels don't fit a Pherni coming-soon |
| 2026-06-13 | Header kept faithful (SHOP / PHERNI / SEARCH (0)), non-functional | "Precisely like this" for the design; only the footer was scoped to minimize |
| 2026-06-13 | White logo rendered black in the header | Pure-white asset is invisible on St. Agni's white bar; black matches the reference wordmark |
| 2026-06-13 | `Discover` dropped under the caption | Nothing to discover on a coming-soon; `Coming Soon` takes the `Fall Winter 26` slot |
| 2026-06-13 | Host on GitHub Pages, DNS at GoDaddy (records handed to Founder) | Free hosting; no credentials shared |

## 12. Relationships

- `pherni` (sibling folder) — a parallel session; untouched, unread.
- GitHub Pages (host) · GoDaddy (registrar for pherni.com) — external systems, Phase 2.

## Version History

| Version | Date | Change |
|---------|------|--------|
| 1.0.0 | 2026-06-13 | Initial creation. Phase 1 built + verified (desktop 1440 + mobile 375). |
