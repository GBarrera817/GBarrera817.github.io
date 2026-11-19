---
name: Gabriela Barrera Ángel
description: Portafolio de una página editado como un single japonés en formato físico, con obi, booklet y tracklist.
colors:
  ultra: "#1b2fd0"
  ultra-deep: "#1423a6"
  obi: "#e4f33b"
  ink: "#0c0f24"
  paper: "#f5f7ff"
  paper-2: "#c9d0ff"
  rule: "#6f7fe6"
typography:
  display:
    fontFamily: "Archivo, Obi Kana, sans-serif"
    fontSize: "clamp(3.1rem, 8.4vw, 6rem)"
    fontWeight: 850
    lineHeight: 0.9
    letterSpacing: "-0.035em"
  track-numeral:
    fontFamily: "Archivo, Obi Kana, sans-serif"
    fontSize: "4.2rem"
    fontWeight: 850
    lineHeight: 0.82
    letterSpacing: "-0.04em"
    fontFeature: "tnum"
  headline:
    fontFamily: "Archivo, Obi Kana, sans-serif"
    fontSize: "clamp(1.9rem, 4vw, 2.8rem)"
    fontWeight: 800
    lineHeight: 1
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Archivo, Obi Kana, sans-serif"
    fontSize: "1.45rem"
    fontWeight: 750
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Zen Kaku Gothic New, Obi Kana, system-ui, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "Archivo, Obi Kana, sans-serif"
    fontSize: "0.78rem"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.08em"
  kana:
    fontFamily: "Obi Kana, Archivo, sans-serif"
    fontSize: "min(4.6rem, 5.6vw, 5.4vh)"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: "0.02em"
rounded:
  none: "0px"
spacing:
  xs: "6px"
  sm: "12px"
  md: "24px"
  lg: "56px"
  xl: "72px"
  gutter: "clamp(20px, 5vw, 72px)"
  obi-width: "clamp(220px, 23vw, 320px)"
components:
  obi-link:
    backgroundColor: "{colors.obi}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "11px 12px"
  obi-link-hover:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.obi}"
  track-number:
    backgroundColor: "{colors.ultra}"
    textColor: "{colors.paper}"
    typography: "{typography.track-numeral}"
    padding: "6px 4px 2px"
  track-number-active:
    backgroundColor: "{colors.obi}"
    textColor: "{colors.ink}"
  badge:
    textColor: "{colors.paper-2}"
    rounded: "{rounded.none}"
    padding: "3px 8px"
  badge-public:
    backgroundColor: "{colors.obi}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "3px 8px"
  credits-panel:
    backgroundColor: "{colors.ultra-deep}"
    textColor: "{colors.paper}"
    padding: "64px clamp(20px, 5vw, 72px) 40px"
---

# Design System: Gabriela Barrera Ángel

## Overview

**Creative North Star: "The First-Press Single"**

The site is a Japanese CD single in its physical edition. A lemon-yellow obi wraps the left edge of the sleeve; everything else is the booklet, printed edge to edge in saturated ultramarine with white ink. Content is not arranged as a landing page but as a release: the obi carries name, trade and contact; the booklet front carries the name at cover scale; the body is a tracklist split into discs (projects, experience), liner notes, and a back-cover credits panel.

The world is flat print. Depth comes only from paper changes (ultramarine booklet, deeper ultramarine back cover, yellow obi) and from fine printer's rules, catalog codes (GBA-2026) and registration marks. Latin display is a heavy wide grotesk (Archivo) the way Japanese pressings set alphabet titles; every kana and kanji is a 900-weight Japanese gothic. Track numbers are set monumentally, never as bullets.

Density is editorial: generous vertical rhythm between discs, tight internal rows, one long measure (62ch) for body copy. Motion is sparse and mechanical, like a player display: the obi slides on once, and a hovered or focused track inverts its number and runs a progress bar once.

**Key Characteristics:**
- Full-bleed ultramarine booklet with white ink; no white page anywhere.
- Vertical lemon obi, full viewport height and sticky on desktop; a horizontal top band on mobile.
- Tracklist rows: monumental numeral, title and note, right-aligned side column.
- Printer's furniture as native ornament: hairline rules, registration marks, catalog codes, the 初回限定盤 sticker.
- Square corners everywhere; zero shadows.

## Colors

Two inks on two papers: ultramarine booklet with white ink, lemon obi with near-black ink.

### Primary
- **Booklet Ultramarine** (ultra): The page itself. Every booklet surface, the theme color and the scrollbar track's partner. It is a surface, not an accent.
- **Back-Cover Ultramarine** (ultra-deep): The credits panel (booklet back cover) and the scrollbar track. Signals the end of the release.

### Secondary
- **Obi Lemon** (obi): The obi paper, the second line of the cover name, kana tags beside headings, the notes headings, the inverted track number, the track progress bar, the public-repo badge, the email in credits, focus rings and text selection. The only accent on ultramarine.

### Neutral
- **White Ink** (paper): Primary text on ultramarine, the heavy 3px disc-head and credits rules, registration marks.
- **Tinted White** (paper-2): Secondary text on ultramarine (metadata, side column, dim notes, catalog strip), the private badge outline. Tinted toward the blue so it reads as printed, not grey.
- **Rule Blue** (rule): Hairline rules between tracks, notes columns, catalog strip and colophon; the "/" separators in the skills line. Decorative only; never text.
- **Obi Ink** (ink): All text and borders on the obi; the 初回限定盤 sticker ground; text on any yellow fill.

### Named Rules
**The Two Papers Rule.** A surface is either ultramarine (booklet) or lemon (obi). Yellow fills on ultramarine are small and earned (an active track number, a public badge); never a yellow section on the booklet.

**The Ink Pairing Rule.** On ultramarine, text is paper, paper-2 or obi. On lemon, text is ink. Ink never appears on ultramarine except inside a yellow fill.

## Typography

**Display Font:** Archivo (variable 100-900, with Obi Kana fallback)
**Body Font:** Zen Kaku Gothic New 400/700 (with Obi Kana, system-ui)
**Kana Font:** Obi Kana, a subset of Zen Kaku Gothic New 900 holding only the kana/kanji used

**Character:** A wide Western grotesk for every Latin heading and numeral, a Japanese gothic for body and every Japanese glyph. Heavy, tightly tracked display against calm, open body text.

### Hierarchy
- **Display** (850, clamp 3.1-6rem, 0.9): The cover name only. Second line in obi lemon. `text-wrap: balance`.
- **Track numeral** (850, 4.2rem, 0.82, tabular; 2.8rem on mobile): Generated `01`, `02`... with leading zero via CSS counter.
- **Headline** (800, clamp 1.9-2.8rem, 1): Disc titles ("Disc 1 · Proyectos") followed by a kana tag in obi lemon at max(1.15rem, 0.62em), tracked 0.06em.
- **Email** (800, clamp 1.5-3.4rem, 1.05): The credits email, set as a headline in obi lemon.
- **Title** (750, 1.45rem, 1.15): Track titles.
- **Obi catchcopy** (800, 1.25rem, 1.3): The obi's one-line pitch, with a 500 0.92rem body-font explanation beneath.
- **Body** (400, 1.05rem, 1.65): Track descriptions and notes, max 62ch. Notes secondary text at 0.95rem in paper-2.
- **Label** (600-800, 0.78-0.85rem, 0.04-0.1em, uppercase): Catalog strip, obi top line, disc-head count, side column metadata, notes headings, colophon.
- **Kana** (900, vertical-rl): The obi's katakana name set tategaki at min(4.6rem, 5.6vw, 5.4vh); horizontal on mobile.

### Named Rules
**The Script Split Rule.** Latin headings and numerals are Archivo; every kana/kanji is Obi Kana 900. Never set Japanese in Archivo or Latin display in the gothic.

**The Monumental Numeral Rule.** List ordinals are track numbers at display scale (4.2rem desktop), never small bullets or chips.

## Layout

Desktop is a two-column page: the obi column (clamp(220px, 23vw, 320px)) sticky at full viewport height, and the booklet filling the rest with a side gutter of clamp(20px, 5vw, 72px). The booklet opens with a catalog strip (registration marks, "Portafolio · 2 discos", "Edición 2026") over a hairline, then the cover, then discs.

Discs are separated by 56px top padding; each starts with a disc-head (headline left, uppercase count right) closed by a 3px white rule. Track rows are a three-column grid (5.4rem numeral / 1fr content / minmax(9rem, auto) side), 22-24px vertical padding, hairline-separated. Notes are three equal columns split by hairlines. Credits bleed to the booklet's edges on ultra-deep with a 3px white top rule.

At 860px and below the page becomes one column: the obi turns into a top band (not sticky), catchcopy explanation hidden, contacts in a three-up grid; the booklet gutter is 16px; track rows collapse to numeral + content with the side column moved under the content and left-aligned; notes stack with horizontal hairlines.

## Elevation & Depth

Flat. No `box-shadow` anywhere. Depth is paper: the obi sits physically over the booklet by color and by stickiness, and the back cover is a darker ultramarine. Rule weight carries hierarchy: 1px rule-blue hairlines inside a section, 3px white rules at section heads and the credits edge.

### Named Rules
**The Printed Matter Rule.** Nothing floats. Hierarchy comes from paper color and rule weight, never shadow or blur.

## Shapes

Every corner is square (no border-radius declared). Outlines are hard: 2px ink borders on obi contact buttons, 1px borders on badges. Registration marks (circle with crosshair, 18px) and a square-capped diagonal arrow are the only drawn glyphs, both inline SVG symbols in currentColor.

## Components

### Obi Contact Buttons
Stamped, utilitarian.
- **Shape:** Square, 2px ink border, 11px 12px padding, label left and arrow right.
- **Default:** Transparent on obi, ink text, Archivo 700 0.95rem.
- **Hover / Focus:** Inverts to ink fill with lemon text (0.25s ease-out-expo). Focus ring on the obi is ink instead of lemon.
- **Mobile:** Three equal columns, centered labels, 0.88rem.

### Track Row (signature)
A tracklist line.
- **Structure:** Counter numeral / title + description (+ optional dim note) / side column (bold primary fact such as stack or years, then uppercase secondary metadata, then a badge).
- **Hover / Focus-within:** The numeral inverts to a lemon block with ink text (0.3s); a 3px lemon progress bar sweeps the bottom edge left to right over 1.4s, once. On leave it resets without animating.
- **Links:** Only public repos link; the title carries the arrow glyph and underlines on hover. Private projects are plain titles.

### Badges
- **Public repo:** Lemon fill, ink text, lemon border.
- **Private:** Transparent, paper-2 text and 1px paper-2 border.
- Both uppercase label type inside the side column, 3px 8px padding, square.

### Disc Head
Headline with an obi-lemon kana tag, an uppercase paper-2 count or date range on the right, and a 3px white rule beneath.

### Credits
Back-cover panel on ultra-deep: headline, the email as a lemon headline link (3px underline on hover), inline LinkedIn/GitHub links with arrows, and a colophon line between registration marks over a hairline.

### Obi
Lemon full-height band: catalog code and place on top (uppercase label), tategaki katakana name beside a vertical ink 初回限定盤 sticker, catchcopy, then contacts. Enters with a top-down clip-path reveal (0.9s, cubic-bezier(.16, 1, .3, 1)).

## Do's and Don'ts

### Do:
- **Do** keep the booklet ultramarine (#1b2fd0) full-bleed with white-ink text; use ultra-deep only for the back-cover credits panel.
- **Do** present any list of work as track rows with CSS-counter numerals at display scale and a right-hand side column.
- **Do** use lemon (#e4f33b) as the single accent on ultramarine, and ink (#0c0f24) as the only text color on lemon.
- **Do** set Latin display in Archivo 750-850 with negative tracking and every Japanese glyph in Obi Kana 900; add new kana only by regenerating the subset.
- **Do** use printer's furniture (hairline rules, registration marks, catalog codes) as the ornament vocabulary.
- **Do** keep every corner square and every surface flat.
- **Do** honor `prefers-reduced-motion`: no obi reveal, no track transitions.

### Don't:
- **Don't** add shadows, blur, gradients or rounded corners.
- **Don't** use rule blue (#6f7fe6) for text; it is too low-contrast on ultramarine.
- **Don't** place yellow sections or large yellow fills on the booklet; yellow on ultramarine stays small and stateful.
- **Don't** turn tracks into equal cards or technology chips.
- **Don't** use emoji or icon fonts; glyphs are inline SVG symbols in currentColor.
