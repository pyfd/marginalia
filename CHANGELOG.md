# marginalia — Changelog

> Started: 19 August 2026

---

## 22 August 2026
- Canonical page: **self-exclusion opt-out for CF Web Analytics** (`?notrack=1`). CF Web Analytics
  (the free JS-beacon product — all that's available on GitHub Pages, un-proxied) has **no**
  IP/visitor filter, so the author's own visits were counting. The beacon is now injected at
  runtime and skipped for opted-out browsers: visit `…/claude-code-setup/?notrack=1` once to
  persist an `mg_notrack` localStorage flag, and thereafter the beacon never fires in that browser
  (per-browser, survives across visits). Falls through and loads normally if localStorage is
  blocked. Only the beacon block changed; page content byte-identical otherwise. [Claude on Pixel-8]
- Pre-HN framing fix (settled over two rounds with Paul): standfirst + intro reworded. "Letting
  Claude Code build its own tooling" read as CC clamouring and Paul merely permitting; the interim
  "building it together" overstated joint coding. Final, accurate shape: **"Five months of Claude
  Code building its own tooling, steered by me"** / intro "having the assistant build its own
  tooling". og:description matches. Rebuilt `published/claude-code-setup/index.html`. [Claude on Fam1]

## 21 August 2026
- Canonical page: **giscus comments** (GitHub Discussions on this repo, category Announcements,
  pathname mapping, theme follows reader's scheme) + closing line reworked to point at them
  ("comments are open below, or over on the demo repo") — "questions welcome" previously had
  no landing spot on the static page. Discussions enabled via API; giscus app install pending
  Paul's GitHub sign-in. [Claude on Fam1]
- Canonical page: social-share card metadata added (`og:title/description/url/image` +
  `twitter:card`, reusing the dev.to cover art — link previews on LinkedIn/Slack/X now show
  a card instead of nothing) and a slim masthead (marginalia mark + wordmark linking back
  to the index — the page previously had no route home). Deliberately NO full hero image:
  text-first is the credibility for the HN audience. [Claude on Fam1]
- LAUNCH DAY (part 1): dev.to mirror flipped live (`published: true` via the dashboard —
  article 4436903 → dev.to/paul_topham_pyfd). Canonical page polished for launch: DRAFT v9
  banner removed, text column widened 40→46rem for desktop reading. HN post planned for
  Monday 24 Aug ~13:00–15:00 BST. [Claude on Fam1]

## 19 August 2026
- Public home for published pieces. Working drafts, version history and the build tooling
  live in a separate private repo (`marginalia-drafts`), so readers only ever see finished work.
- Added `img/cover.png` (+ SVG source): the dev.to cover for the first piece — the marginalia
  margin-note mark on a dark dot-grid, with the series title. Hotlinked from the article's front matter.
- Published the first piece — "How I built a Claude Code system that actually knows how I work" —
  as the styled, self-contained canonical page under `published/claude-code-setup/`, served via
  GitHub Pages. Added a root landing `index.html` listing pieces and linked the piece from the
  README. dev.to becomes a mirror pointing back here via `canonical_url`. [Claude on Pixel-8]
- Added the Cloudflare Web Analytics beacon to the canonical page so visits/clicks are measured
  before we drive HN/dev.to traffic (JS-beacon site on hostname `pyfd.github.io`; token is public
  by design). Rebuilt `published/claude-code-setup/index.html`. [Claude on Pixel-8]
