# PHERNI — Coming Soon

A single-page coming-soon site, styled as a precise clone of the St. Agni homepage
(`https://int.st-agni.com/`). Static HTML/CSS, no build step, no dependencies.

## Files
- `index.html` — the page (inline CSS, no JS framework)
- `assets/banner.jpg` (2560w) + `assets/banner-mobile.jpg` (1280w) — hero, `srcset`-swapped
- `assets/logo-black.png` — PHERNI wordmark, black (for the white header)
- `assets/logo.png` — PHERNI wordmark, white (original; for dark backgrounds)
- `_src/banner-original.png` — the 15 MB master (git-ignored; not deployed)
- `.nojekyll` — serve `assets/` untouched on GitHub Pages
- `CNAME` — created at deploy: contains `pherni.com`

## Local preview
```
python3 -m http.server 4137 --directory .
# open http://localhost:4137
```

## Deploy — GitHub Pages + pherni.com (Phase 2)
1. `git init`, commit `index.html` + `assets/` + `.nojekyll` + `CNAME` (= `pherni.com`).
2. Push to a public repo (proposed: `pherni-coming-soon`), branch `main`.
3. Repo **Settings → Pages**: Source = `main` / root; Custom domain = `pherni.com`; Enforce HTTPS.
4. **GoDaddy DNS** (apex `pherni.com`):
   ```
   A     @     185.199.108.153
   A     @     185.199.109.153
   A     @     185.199.110.153
   A     @     185.199.111.153
   CNAME www   <github-username>.github.io
   ```
   Remove any conflicting parked A/CNAME records first. (Optional IPv6 AAAA `@`:
   `2606:50c0:8000::153`, `8001::153`, `8002::153`, `8003::153`.)
5. Verify: `curl -I https://pherni.com` → 200; `www` redirects to apex; HTTPS lock green.
   (DNS + cert can take minutes to ~48h.)
