# marginalia — Changelog

> Started: 19 August 2026

---

## 21 August 2026
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
