[README.md](https://github.com/user-attachments/files/27428179/README.md)
# Before the Fall — STEADI Pilot Study

**Community-Based STEADI Screening to Identify Hidden Fall Risk Before ED Presentation**

A research landing page for a pilot implementation study presented at OHSU EM Scholarship Day.

🔗 **Live page:** https://nate-stanley.github.io/before-the-fall/

---

## Repository Structure

```
/
├── index.html          # Single-file landing page (all CSS + JS inline)
├── Poster.pdf          # Research poster (linked from Downloads bar)
├── abstract.pdf        # Study abstract (linked from Downloads bar + abstract section)
├── README.md           # This file
└── img/
    ├── hero.jpg        # Hero background photo (dusk tram, Portland)
    ├── ohsu-logo.png   # OHSU full-color logo, transparent background
    ├── stanley.jpg     # Headshot — Nathaniel Stanley (optional, falls back to initials)
    ├── kea.jpg         # Headshot — Bory Kea
    ├── rosz.jpg        # Headshot — Ren Rosz
    ├── kiyoshi.jpg     # Headshot — Hiroko Kiyoshi-Teo
    ├── gold.jpg        # Headshot — Sarah Gold
    ├── wong.jpg        # Headshot — Heather Wong
    ├── berryhill.jpg   # Headshot — Jody Berryhill
    ├── brown.jpg       # Headshot — Rebecca Brown
    └── riley.jpg       # Headshot — Nicole Riley
```

---

## Image Asset Status

| File | Description | Status |
|------|-------------|--------|
| `img/hero.jpg` | Dusk tram photo — Portland skyline with Mt. Hood | **Required — upload to repo** |
| `img/ohsu-logo.png` | OHSU logo — full color, transparent PNG (`OHSU-RGB-4C-POS.png`) | **Required — upload to repo** |
| `img/stanley.jpg` | Headshot — Nathaniel Stanley | ⏳ Pending |
| `img/kea.jpg` | Headshot — Bory Kea | ⏳ Pending |
| `img/rosz.jpg` | Headshot — Ren Rosz | ⏳ Pending |
| `img/kiyoshi.jpg` | Headshot — Hiroko Kiyoshi-Teo | ⏳ Pending |
| `img/gold.jpg` | Headshot — Sarah Gold | ⏳ Pending |
| `img/wong.jpg` | Headshot — Heather Wong | ⏳ Pending |
| `img/berryhill.jpg` | Headshot — Jody Berryhill | ⏳ Pending |
| `img/brown.jpg` | Headshot — Rebecca Brown | ⏳ Pending |
| `img/riley.jpg` | Headshot — Nicole Riley | ⏳ Pending |

> **Note:** The page gracefully falls back to initials circles if headshot files are missing. No placeholder or broken image will appear.

---

## Pending Items

- [ ] Upload `img/hero.jpg` and `img/ohsu-logo.png` to the `img/` folder
- [ ] Collect and upload headshots (9 team members, named per table above)
- [ ] Generate QR code pointing to `https://nate-stanley.github.io/before-the-fall/` and replace placeholder on poster
- [ ] Confirm final poster is `Poster.pdf` (capital P) — the download link is case-sensitive on GitHub Pages

---

## Design System

**Colors**
| Variable | Hex | Use |
|----------|-----|-----|
| `--navy` | `#1A4480` | Primary — headers, borders, backgrounds |
| `--blue` | `#2962A8` | Medium — links, active states |
| `--steel` | `#6B9FC7` | Light — eyebrow text, accents |
| `--gold` | `#F2AA28` | Accent — section labels, author names, highlights |
| `--muted` | `#5A7B9B` | Secondary text |
| `--bg` | `#F2F6FB` | Page background |
| `--pale` | `#EEF5FB` | Card/callout backgrounds |

**Typography**
- `DM Serif Display` (Google Fonts) — hero title and large stat numbers only
- `Georgia` — all body text
- Section labels: uppercase, letter-spaced, `0.625rem`, gold underline

**Layout**
- Content column: `860px` base / `920px` on desktop (≥1200px)
- Section padding: `36px` mobile / `52px` desktop

---

## Technical Notes

**Hosting:** GitHub Pages — deploys automatically from `main` branch root.

**Fonts:** Loaded from Google Fonts CDN. Requires internet connection to render correctly; falls back to Georgia.

**Analytics:** GoatCounter — privacy-friendly, no cookies.
- Dashboard: https://nstanley.goatcounter.com
- The tracking script loads asynchronously and does not affect page performance.

**Accessibility:** Font sizes use `rem` units and respect browser/OS accessibility font-size settings. Base is `html { font-size: 100% }`.

**No build step required.** `index.html` is fully self-contained — all CSS and JavaScript are inline. Edit directly and push.

---

## Updating Content

All content is in `index.html`. Key sections by line reference:

| Section | What to edit |
|---------|-------------|
| Hero finding text | `.hero-finding` paragraph in `<header>` |
| Key findings cards | `#findings` section — edit `.num`, `.lbl`, `.sub` values |
| Study at a Glance | `#overview` section — `<dl>` key/value pairs |
| Why This Matters | `#meaning` section — `.callout` paragraphs |
| Abstract | `#abstract` section — inside `<details>` |
| Team bios | `#team` section — `.person` blocks |
| References | Final `<section>` before `</main>` |

---

## Study Information

**IRB:** STUDY00026434  
**Funding:** OHSU Trauma Program (screening events); REDCap UL1TR002369  
**Presented at:** OHSU EM Scholarship Day  

**Presenting author:** Nathaniel Stanley, BS — stanlnat@ohsu.edu  
**Principal investigator:** Bory Kea, MD, MCR, FACEP — kea@ohsu.edu
