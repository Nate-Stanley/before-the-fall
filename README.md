# Before the Fall — STEADI Pilot Study

**Community-Based STEADI Screening to Identify Hidden Fall Risk Before ED Presentation**

A mobile-first research landing page for the OHSU EM Scholarship Day poster presentation. The page is intended to support the poster QR code by giving viewers a polished companion site with the key findings, study overview, poster PDF, abstract, education videos, resources, and study-team information.

Live site: <https://nate-stanley.github.io/before-the-fall/>

---


## Fall Prevention Toolkit additions

This version includes a locally hosted OHSU booklet and externally linked CDC STEADI tools. The OHSU booklet should remain at:

```text
files/fall-risk-assessment-event-booklet.pdf
```

CDC PDFs/resources are linked externally so the site points users to current CDC-hosted materials rather than duplicating federal documents in the repository.

## Repository Structure

```text
/
├── index.html              # Single-file landing page; all CSS and JS are inline
├── Poster.pdf              # Final poster PDF linked from the hero button
├── abstract.pdf            # Abstract PDF linked from the abstract section
├── README.md               # This file
└── img/
    ├── hero-desktop.jpg    # Desktop hero image crop
    ├── hero-mobile.jpg     # Mobile hero image crop
    ├── og-image.jpg        # Social/link preview image
    ├── favicon.svg         # Browser tab icon
    ├── ohsu-logo.png       # OHSU logo used in hero/footer
    ├── stanley.jpg         # Optional headshot; falls back to initials if missing
    ├── kea.jpg             # Optional headshot; falls back to initials if missing
    ├── rosz.jpg            # Optional headshot; falls back to initials if missing
    ├── kiyoshi.jpg         # Optional headshot; falls back to initials if missing
    ├── gold.jpg            # Optional headshot; falls back to initials if missing
    ├── wong.jpg            # Optional headshot; falls back to initials if missing
    ├── berryhill.jpg       # Optional headshot; falls back to initials if missing
    ├── brown.jpg           # Optional headshot; falls back to initials if missing
    └── riley.jpg           # Optional headshot; falls back to initials if missing
```

GitHub Pages is case-sensitive. The files must be named exactly as shown above.

---

## Required Files

These files are required for the page to render correctly:

| File | Purpose |
|---|---|
| `index.html` | Main landing page |
| `Poster.pdf` | Opens from the **View Poster** button |
| `abstract.pdf` | Opens from the abstract section |
| `img/hero-desktop.jpg` | Desktop hero background |
| `img/hero-mobile.jpg` | Mobile hero background |
| `img/og-image.jpg` | Link preview image for texts/social shares |
| `img/favicon.svg` | Browser tab icon |
| `img/ohsu-logo.png` | OHSU mark in the hero/footer |

Headshots are optional. If an image is missing, the page displays an initials fallback instead of a broken image.

---

## Uploading to GitHub Pages

1. Confirm GitHub Pages is publishing from the correct source:
   - **Settings → Pages → Build and deployment**
   - Source should match where `index.html` is located, usually the root of the `main` branch.

2. Upload or replace these files in the repository root:
   - `index.html`
   - `Poster.pdf`
   - `abstract.pdf`
   - `README.md`

3. Upload or replace these files in `/img/`:
   - `hero-desktop.jpg`
   - `hero-mobile.jpg`
   - `og-image.jpg`
   - `favicon.svg`
   - `ohsu-logo.png`
   - optional headshots

4. Commit changes.

5. Wait for GitHub Pages to redeploy.

6. Test the live page in an incognito/private window:
   - <https://nate-stanley.github.io/before-the-fall/>

---

## Quick QA Checklist

Before sharing the QR code broadly, confirm the following on both desktop and phone:

- Hero image loads and Mt. Hood is visible.
- OHSU logo appears inline with the event label.
- **View Poster** opens `Poster.pdf`.
- **Contact Presenter** opens an email to the presenting author.
- Key findings display correctly:
  - 66% high risk
  - 1 in 2 did not perceive elevated fall risk
  - 45% discussed fall prevention with a PCP
  - 83% had low concern about falling
- **From Screening to Action** pathway is readable on mobile.
- **Why This Matters** appears visually emphasized but not overdesigned.
- **Screening & Measures** accordion opens/closes properly.
- Abstract accordion opens/closes properly and links to `abstract.pdf`.
- YouTube videos load.
- Resource links open in a new tab.
- Team dropdowns open/close properly.
- Footer logo and contact text are visible.
- No broken images appear.

---

## Mobile Testing

The site is designed mobile-first for QR-code use. For testing:

1. Open the live page on a real phone.
2. Test both portrait and landscape orientation.
3. Test at least one mobile browser, ideally Chrome or Firefox/Samsung Internet.
4. Check the hero crop, button tap targets, card spacing, accordions, videos, and PDF links.

For desktop simulation:

- Chrome/Edge: `F12` → device toolbar icon.
- Firefox: `Ctrl + Shift + M` for Responsive Design Mode.

Suggested test widths:

```text
360px
390px
412px
430px
768px
1024px
1440px
```

---

## Temporary Preview Without GitHub

If GitHub Actions/Pages is delayed, preview with Netlify Drop:

1. Go to <https://app.netlify.com/drop>.
2. Drag in the full project folder, not only `index.html`.
3. Confirm the folder includes:

```text
index.html
Poster.pdf
abstract.pdf
img/
```

Netlify will generate a temporary preview URL for QA.

---

## Design System

### Color Palette

| Token | Hex | Use |
|---|---:|---|
| `--navy` | `#1A4480` | Primary headings, stats, card rules |
| `--navy-dark` | `#0E294F` | Hero overlay and deep accents |
| `--blue` | `#2962A8` | Link hover and secondary accents |
| `--steel` | `#6B9FC7` | Muted blue accent |
| `--gold` | `#F2AA28` | Primary CTA, section underline, key emphasis |
| `--gold-dark` | `#D4930F` | Gold hover/secondary accent |
| `--bg` | `#F3F7FB` | Page background |
| `--card` | `#FFFFFF` | Card backgrounds |
| `--text` | `#1D2D3D` | Body text |
| `--muted` | `#5B7188` | Secondary text |
| `--line` | `#D4E1EF` | Borders and dividers |

### Typography

The page uses Google Fonts:

- **Source Sans 3** — body text, buttons, navigation, labels, cards
- **Source Serif 4** — hero title and key-finding numbers

This pairing was chosen to keep the page professional and legible while preserving an editorial academic feel.

### Layout Notes

- The hero uses separate desktop and mobile image crops.
- Most content lives inside a centered column with a max width of approximately `940px`.
- The desktop page includes a right-side section navigation.
- The mobile page hides the side navigation and prioritizes a linear reading flow.
- Most content blocks share the same card radius, border, and shadow system for visual cohesion.

---

## Main Content Sections

| Section | Purpose |
|---|---|
| Hero | Page title, key takeaway, author/PI, poster/contact actions |
| Key Findings | Four high-level findings from the poster |
| Study at a Glance | Design, setting, sample, period, IRB |
| From Screening to Action | Simplified community screening pathway |
| Why This Matters | Interpretive implication and future direction |
| Study Details | Collapsed screening/measures and full abstract |
| Patient Education Videos | Required OHSU fall-prevention video embeds |
| Resources | CDC/OHA/OHSU fall-prevention links |
| Study Team | Primary contacts visible; additional team members in dropdowns |
| Acknowledgments / References | Funding, REDCap, volunteer/team acknowledgment, references |

---

## Updating Content

All site content is in `index.html`.

Common edits:

| To edit | Search for |
|---|---|
| Hero takeaway | `class="hero-finding"` |
| Key finding cards | `id="findings"` |
| Study overview | `id="overview"` |
| Pathway labels | `id="model"` |
| Why This Matters | `id="meaning"` |
| Screening details | `Screening &amp; Measures` |
| Abstract text | `Read the full abstract` |
| Videos | `id="videos"` |
| Resources | `id="resources"` |
| Team bios | `id="team"` |
| References | `id="refs"` |

---

## Headshot Naming

Headshot images should be square or close to square and placed in `/img/`.

Use these exact filenames:

```text
stanley.jpg
kea.jpg
rosz.jpg
kiyoshi.jpg
gold.jpg
wong.jpg
berryhill.jpg
brown.jpg
riley.jpg
```

If a headshot is missing, the HTML uses an initials fallback. This prevents broken-image icons from appearing.

---

## Technical Notes

- No build step is required.
- No npm, bundler, framework, or deployment script is needed.
- CSS and JavaScript are inline inside `index.html`.
- The page uses relative paths, so it works on GitHub Pages, Netlify Drop, and local previews.
- The page includes Open Graph and Twitter preview metadata.
- `og-image.jpg` is referenced using the public GitHub Pages URL.
- The favicon is an SVG file at `img/favicon.svg`.
- YouTube videos are embedded with standard iframe embeds.
- GoatCounter analytics may be included asynchronously if present in the deployed version.

---

## Troubleshooting

### The old README renders instead of the site

Make sure `index.html` exists in the GitHub Pages publishing folder. If `index.html` is missing, GitHub Pages may render `README.md` instead.

### The hero image does not load

Check exact filenames and paths:

```text
img/hero-desktop.jpg
img/hero-mobile.jpg
```

### Poster or abstract links do not work

Check exact capitalization:

```text
Poster.pdf
abstract.pdf
```

### GitHub Actions is stuck waiting for a runner

That usually indicates a GitHub-hosted runner/Actions queue issue, not an HTML issue. Use Netlify Drop for temporary QA while waiting.

### Link preview image does not update

Social apps cache Open Graph images. Wait or use a link-preview debugger to refresh the cached preview.

---

## Study Information

**IRB:** STUDY00026434  
**Presented at:** OHSU EM Scholarship Day  
**Funding/Acknowledgment:** Screening events funded by the OHSU Trauma Program. Study data managed using REDCap (UL1TR002369).  

**Presenting author:** Nathaniel Stanley, BS — stanlnat@ohsu.edu  
**Principal investigator:** Bory Kea, MD, MCR, FACEP — kea@ohsu.edu
