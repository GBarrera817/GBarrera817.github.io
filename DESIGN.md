---
name: Gabriela Barrera Ángel
description: Portafolio de una página que es una sesión de terminal; se explora escribiendo comandos.
colors:
  phosphor-black: "#0b100d"
  phosphor-black-raised: "#111a15"
  phosphor-text: "#c4f2d0"
  prompt-green: "#4ee38a"
  moss-dim: "#7a9a85"
  amber: "#ffb547"
  error-red: "#ff7a6b"
  grid-line: "#22332a"
typography:
  body:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.6
  body-strong:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "15px"
    fontWeight: 700
    lineHeight: 1.6
  prompt:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "max(16px, 1em)"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.6
  status:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1
  ascii-logo:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "40px"
    fontWeight: 700
    lineHeight: 1
  ascii-logo-sm:
    fontFamily: "JetBrains Mono, ui-monospace, Cascadia Mono, Consolas, monospace"
    fontSize: "15px"
    fontWeight: 700
    lineHeight: 1
rounded:
  none: "0px"
spacing:
  gutter: "clamp(16px, 3vw, 40px)"
  screen-top: "20px"
  block: "14px"
  chip-gap: "8px"
  frame-body-y: "6px"
  frame-body-indent: "2ch"
  column-gap: "24px"
  fetch-gap: "32px"
components:
  command-chip:
    backgroundColor: "{colors.phosphor-black-raised}"
    textColor: "{colors.phosphor-text}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "5px 12px"
  command-chip-hover:
    textColor: "{colors.amber}"
  inline-command:
    textColor: "{colors.amber}"
    typography: "{typography.body}"
    padding: "0"
  prompt-input:
    textColor: "{colors.phosphor-text}"
    typography: "{typography.prompt}"
    padding: "0"
  block-cursor:
    backgroundColor: "{colors.amber}"
    width: "1ch"
    height: "1.2em"
  cat-frame:
    textColor: "{colors.moss-dim}"
    typography: "{typography.body}"
    padding: "6px 0 6px 2ch"
    width: "72ch"
  listing-header:
    textColor: "{colors.moss-dim}"
    typography: "{typography.body}"
  tmux-status-bar:
    backgroundColor: "{colors.prompt-green}"
    textColor: "{colors.phosphor-black}"
    typography: "{typography.status}"
    padding: "5px clamp(16px, 3vw, 40px)"
---

# Design System: Gabriela Barrera Ángel

## Overview

**Creative North Star: "La sesión abierta"**

The whole site is one full-height terminal session on green-black. There is no landing page underneath it: no hero, no card grid, no navigation bar. Content exists only as the output of commands (`neofetch`, `ls`, `cat`, `exp`, `estudios`, `contacto`), appended to a scrolling log above a live prompt. The visitor reads by typing or by clicking command names that appear inside earlier output, exactly as a session's history accumulates.

The material is phosphor text on a near-black screen, quiet rather than cinematic. Green belongs to the system (prompt, status bar), amber marks anything the visitor can name or run and the cursor itself, red appears only when a command fails. One monospace family, two weights, almost one size: hierarchy comes from color and position in the log, not from scale. The single exception is the neofetch block logo, which is drawn large because it is a picture, not a heading. Depth is flat; structure inside output is drawn with box-drawing glyphs (`┌─`, `└─`, `─`), never with filled panels. The frame is fixed: scrolling screen, a row of suggested commands, and a tmux-style status bar pinned to the bottom with the session name and La Serena time.

Density is that of a real terminal: tight line rhythm (1.6), small fixed gaps between output blocks, tabular rows laid out like `ls -l`. Motion is terminal-native and short: an amber block cursor that blinks in hard steps, and on load the word `neofetch` typed into the prompt at 40ms per character before its output appears whole. Under reduced motion the cursor holds solid and the typing is skipped. There is no glow, no scanline, no animated output.

**Key Characteristics:**
- One screen, one log, one prompt; every piece of content is command output.
- JetBrains Mono everywhere (self-hosted, including box, block and arrow glyphs), ligatures off, weights 400 and 700 only.
- Green = system, amber = nameable/runnable and the cursor, red = error, moss = metadata and drawn structure.
- Square corners, box-glyph frames and rules, no filled cards, no shadows, no glow.
- Tmux status bar as the page's only footer.

## Colors

A phosphor palette: one green-black ground, one pale phosphor text, and three signal hues with strictly separated jobs.

### Primary
- **Prompt Green** (prompt-green): the system's own voice. The `gabriela@la-serena` prompt, the neofetch host line, the `público` flag in `ls`, and the full-bleed tmux status bar.

### Secondary
- **Amber** (amber): everything the visitor can name or execute, plus the block cursor. Prompt path `~`, help-table command names, neofetch keys, project names inside `cat` frames, experience dates, row labels in `estudios` and `contacto`, inline runnable commands, links, focus ring, selection, and chip hover.

### Tertiary
- **Error Red** (error-red): failed commands only (`comando no encontrado`, missing project, private repo on `open`, the `sudo` joke).

### Neutral
- **Phosphor Black** (phosphor-black): the screen, the chips row, and the text on the green status bar. Also `theme-color`.
- **Phosphor Black Raised** (phosphor-black-raised): the one raised step, used only behind command chips.
- **Phosphor Text** (phosphor-text): default output and typed input.
- **Moss Dim** (moss-dim): metadata, descriptions in tables, hints, the `:` in the prompt, private flags, column headers, and every drawn glyph structure (`cat` frames, `─` rules, the neofetch rule line).
- **Grid Line** (grid-line): 1px hairlines (chip borders, the chips row top rule) and the scrollbar thumb.

### Named Rules
**The Red Means Failure Rule.** Error Red appears only on a failed or refused command. Never use it for emphasis, status, or decoration.

**The Amber Is Clickable Rule.** If a word is amber inside output, it names something the visitor could type; runnable amber words are real buttons that execute that command. The block cursor is the one amber mark that is not a name: it is where the next name goes.

## Typography

**Display Font:** none; the system has no display face.
**Body Font:** JetBrains Mono (with ui-monospace, Cascadia Mono, Consolas, monospace), self-hosted latin and latin-ext subsets plus a 400 and 700 subset for arrows and box-drawing/block elements (U+2190-21FF, U+2500-259F), all `font-display: swap`, latin preloaded.

**Character:** a single engineer's monospace, ligatures disabled so `->`, `==`, `--` read as typed. Bold is the only typographic emphasis. Box and block glyphs come from the same face, so frames and the logo align on the character grid on every platform.

### Hierarchy
- **Body** (400, 15px, 1.6): all output and project descriptions. `cat` frames cap at 72ch, the log at 980px.
- **Body Small** (400, 14px, 1.6): the whole body under 640px.
- **Body Strong** (700, body size): prompt, neofetch host and keys, names in `whoami` and `exp`, the project name inside a `cat` frame (set at 1em, never enlarged).
- **Prompt** (400, `max(16px, 1em)`): the prompt line, label and input together.
- **Label** (400, 14px): suggested-command chips.
- **Status** (400/700, 13px, line-height 1): tmux status bar; the window name `[portafolio]` is bold.
- **ASCII Logo** (700, 40px, line-height 1; whole-pixel ch so █ cells meet without seams): the block-character "GB" mark in neofetch, amber.
- **ASCII Logo Small** (700, 15px, line-height 1): the same mark under 640px, where neofetch stacks to one column.

### Named Rules
**The One Size Rule.** Headings do not grow. A title is the body size in bold amber; hierarchy is color and log position, never scale. The ASCII logo is an image made of glyphs and is the only text set large.

**The Prompt Input Floor Rule.** The prompt line is never below 16px (`max(16px, 1em)`) so mobile browsers do not zoom on focus.

## Layout

A fixed three-band column filling `100dvh`: the scrolling screen (flex 1), the suggested-commands row, and the status bar. The keyboard resizes the content (`interactive-widget=resizes-content`) so the prompt stays above it.

- Side gutter is shared by all three bands (16px to 40px via `clamp(16px, 3vw, 40px)`); the screen adds 20px top padding.
- Output blocks stack with a 14px bottom margin; the log max-width is 980px.
- Tabular output (`ls`, `help`, `estudios`, `contacto`) uses a max-content grid with 24px column gaps, rows unwrapped except description cells.
- Neofetch is a two-column grid (logo, info) with 6px by 32px gaps; it collapses to one column under 640px.
- The chips row scrolls horizontally with a hidden scrollbar; it never wraps. Chip order is fixed: `help`, `contacto`, `ls`, `whoami`, `exp`, `estudios`, `clear`.
- At 640px and below: body 14px, logo 15px, the `ls` STACK column and secondary tmux segments hide.

## Elevation & Depth

Flat. There are no shadows anywhere. Output never sits on a panel: grouping is drawn with moss box-drawing glyphs on the bare screen. The only tonal step (Phosphor Black to Phosphor Black Raised) is behind command chips, with a 1px Grid Line border. The status bar is the only solid color block, and it is flat green.

### Named Rules
**The No Glow Rule.** No text-shadow, box-shadow, bloom, or neon border. Phosphor is conveyed by color alone.

**The Glyphs Not Panels Rule.** Structure inside the log is drawn with characters a terminal could print (`┌─ name ───`, `└───`, `─`), in Moss Dim. Never a filled or bordered box.

## Shapes

Square corners throughout (0px). Hairlines are 1px Grid Line, used only on chips. All other ornament is terminal-native and drawn in type: the block-character logo, `┌─`/`└─` frames around `cat` output, full-width `─` rules (after the `ls` listing, before `exp` and `estudios` output), a short `─` rule under the neofetch host, and a neofetch color swatch strip of flush 26 by 14px blocks. Rules fill their line by overflowing a long run of `─` and clipping, so they track the column width.

## Components

### Prompt
- **Style:** a label (`gabriela@la-serena:~$`, bold green, `~` amber, `:` moss) followed by a borderless, transparent input in Phosphor Text whose width tracks its content in `ch`, with the native caret hidden. The line is `max(16px, 1em)`. No outline on the input itself; a click anywhere on the screen focuses it.
- **Behavior:** Enter runs, Tab autocompletes commands and project ids, Up/Down walk history, Ctrl+L clears.
- **Boot:** on load the prompt types `neofetch` at 40ms per character, then echoes it and prints the output whole, followed by a moss welcome line with an inline `help`. Under reduced motion the typing is skipped and the output appears at once.

### Block Cursor
An amber 1ch by 1.2em block placed right after the typed text, `aria-hidden`, pointer-transparent. It blinks with `steps(1)` on a 1.06s cycle (hard on/off, no fade). Under `prefers-reduced-motion: reduce` it is solid.

### Inline Command
The signature: a runnable command inside output. Amber text, underlined at 45% amber with 0.2em offset; hover makes the underline solid. It is a real `<button>` with no box, and clicking it executes the command and echoes it to the log.

### Command Chips
- **Style:** Raised background, Phosphor Text, 1px Grid Line border, square, 5px by 12px padding, 14px.
- **Hover:** border and text turn amber. Focus uses the global 2px amber outline at 2px offset.
- Preceded by a moss `prueba:` hint. Order: help, contacto, ls, whoami, exp, estudios, clear.

### Cat Frame
Project detail printed by `cat <proyecto>`, drawn on the bare screen, max 72ch.
- **Top line:** moss `┌─ `, the project name in bold amber, then a `─` rule to the frame width. It is the block's `h2`, at body size.
- **Body:** indented 2ch with 6px above and below; description in Phosphor Text, `stack:` and `repo:` lines in moss with values in Phosphor Text or as links and an inline `open`.
- **Bottom line:** moss `└` plus a `─` rule.
- No background, no border box, no shadow.

### Listing
`ls -l` style rows: a header row of dim uppercase column names (`ACCESO`, `NOMBRE`, `STACK`), then visibility flag (green `público` or moss `privado`), runnable project id with a trailing `/`, moss stack column. Closes with a full-width `─` rule and a moss hint line. `help`, `estudios` and `contacto` use the same grid in two columns, amber keys on the left, without a header row.

### Tmux Status Bar
Full-bleed Prompt Green band, Phosphor Black text, 13px, line-height 1, 5px vertical padding. Left: bold `[portafolio]` and window list; right: initials, city and live time in `America/Santiago`. Decorative (`aria-hidden`), single line, overflow hidden.

### Neofetch
Amber block-letter logo (40px; 15px on mobile) beside an info column: green bold host, moss `─` rule, amber bold keys with plain values, and runnable commands as values where useful, ending with the palette swatch strip.

## Do's and Don'ts

### Do:
- **Do** deliver every new piece of content as the output of a command, echoed after the prompt.
- **Do** make any project or command name that appears in output an Inline Command that runs it.
- **Do** keep green for the system, amber for the nameable and the cursor, red for errors, moss for metadata and drawn structure.
- **Do** group output with moss box-drawing glyphs and `─` rules, the way a CLI prints them.
- **Do** use the global focus ring: 2px amber outline, 2px offset.
- **Do** keep everything in JetBrains Mono at 400 or 700, ligatures off, with box and block glyphs from the self-hosted subset.
- **Do** stop the cursor blink and skip the boot typing under reduced motion.

### Don't:
- **Don't** add a hero, a card grid, or a navigation bar; the session is the only interface.
- **Don't** put output on filled or bordered panels; draw frames with glyphs.
- **Don't** add glow, text-shadow, box-shadow, or bright/neon borders.
- **Don't** round corners.
- **Don't** enlarge headings; titles stay at body size. Only the ASCII logo is set large.
- **Don't** animate output; only the prompt types, and only at boot.
- **Don't** use Error Red for anything but failed commands.
