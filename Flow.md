# Pherni Coming-Soon — Flow

**Document:** `Flow.md`
**Last Cut:** 2026-06-13

---

## 1. Status

Phase 1 DONE + verified (desktop 1440 + mobile 375). Awaiting Founder visual sign-off, then Phase 2 (deploy).

## 2. Active Cut

Phase 1 review — show the Founder the rendered page; confirm before deploy.

## 3. Next Cuts

1. Founder confirms the look (or requests tweaks).
2. Phase 2 — collect creds (GitHub username + push auth; confirm repo name + domain form).
3. `git init` → push to public repo → enable Pages → add `CNAME` (`pherni.com`).
4. Hand the Founder the GoDaddy DNS records; they paste them.
5. Verify `https://pherni.com` (200 + HTTPS + www→apex redirect).

## 4. Open Tensions

- Phase-2 credentials not yet provided (GitHub username, push-auth method). Blocks deploy only.

## 5. Trace Log

- 2026-06-13: Phase 1 built. Project basin `pherni-b` scaffolded; `banner.png`→optimized JPGs (660K/144K), white `LOGO.png`→black header logo; `index.html` = faithful St. Agni clone (fixed header SHOP/PHERNI/SEARCH(0) · full-bleed hero · `Coming Soon` caption · minimized footer). Verified via Claude Preview at 1440×900 and 375×812 — geometry + screenshots confirm faithful layout, centered caption, legible white text over the dark jacket, responsive footer.

## 6. Rejected (Boundary)

- Keeping St. Agni's exact footer labels (boutiques/stockists/loyalty/gift card). Outside boundary — Founder chose Pherni-minimal.
- Third-party chat bubble. Outside boundary — non-functional widget, not part of the design.

## 7. Handoff

Phase 1 complete and verified; the page lives in `index.html` and renders faithfully at desktop + mobile. Resume at Phase 2: get the Founder's GitHub username + chosen push-auth (gh device-flow / PAT / they-add-me), confirm repo name (`pherni-coming-soon`) and that apex `pherni.com` + www-redirect is the target, then init/push/enable-Pages/add-CNAME and hand over the GoDaddy DNS records (in README.md). Local preview server: `python3 -m http.server 4137 --directory <proj>` (or the `pherni` launch.json config).
