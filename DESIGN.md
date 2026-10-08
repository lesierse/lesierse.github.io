---
name: Lesierse IT
description: Application development and consultancy for software, cloud and AI, drawn in architecture-diagram notation.
colors:
  canvas-paper: "#f2f4f7"
  sheet: "#ffffff"
  ink: "#0c1a2b"
  ink-secondary: "#3f4f66"
  rule: "#c9d2de"
  wire: "#5a6b83"
  system-blue: "#1554d1"
  system-blue-deep: "#0f43ad"
  person-navy: "#0a2a5e"
  own-marigold: "#f4b000"
  on-dark: "#ffffff"
  on-dark-secondary: "#dce7fb"
typography:
  display:
    fontFamily: "Archivo, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 3.9vw, 3.5rem)"
    fontWeight: 780
    lineHeight: 1.08
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Archivo, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1.9rem, 3.4vw, 2.85rem)"
    fontWeight: 760
    lineHeight: 1.08
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Archivo, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 740
    lineHeight: 1.08
  body:
    fontFamily: "Archivo, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  notation:
    fontFamily: "Archivo, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: "0.02em"
rounded:
  sm: "4px"
  md: "6px"
  lg: "10px"
  pill: "999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "48px"
  3xl: "72px"
  4xl: "112px"
components:
  button-primary:
    backgroundColor: "{colors.system-blue}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.md}"
    padding: "0 24px"
    height: "48px"
  button-primary-hover:
    backgroundColor: "{colors.system-blue-deep}"
  button-quiet:
    backgroundColor: "{colors.sheet}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "0 24px"
    height: "48px"
  node-system:
    backgroundColor: "{colors.system-blue}"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.md}"
    padding: "16px"
  node-person:
    backgroundColor: "{colors.person-navy}"
    textColor: "{colors.on-dark}"
    padding: "16px"
  node-own:
    backgroundColor: "{colors.own-marigold}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
  chip:
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
    padding: "3px 10px"
    typography: "{typography.notation}"
---

# Design System: Lesierse IT

## Overview

**Creative North Star: "The System Context Diagram"**

Lesierse IT is presented in the notation its buyers already read every day: C4-style architecture diagrams. Boxes are typed (`[Person]`, `[Software studio]`, `[Service: …]`), relationships are dashed and labelled, and groups sit inside dashed system boundaries on a dot-grid canvas. The page says "this person thinks in systems" before a single claim is read.

It refuses the category's default dark-gradient SaaS hero with stock icon cards. Colour is semantic, borrowed from diagram convention: navy is a person, blue is a system, marigold is Lesierse IT's own shipped app (Ace31), white boxes are the client's systems.

**Key Characteristics:**
- Dot-grid canvas paper with white diagram sheets laid on top.
- Every box carries a name, a bracketed type label and optionally a one-line description.
- Dashed relationships with labelled verbs and solid arrowheads.
- One wide, heavy grotesque for statements; the same family narrowed for notation.
- Bilingual (EN at `/`, NL at `/nl/`) with identical structure.

## Colors

Full palette with semantic roles. Each colour owns whole regions, not sprinkled accents.

### Primary
- **System Blue** (`#1554d1`): the Lesierse IT system box, primary buttons, highlighted headline words, the first service container.

### Secondary
- **Person Navy** (`#0a2a5e`): person nodes, the consultancy container and the full contact section.

### Tertiary
- **Own-Product Marigold** (`#f4b000`): reserved for own apps (Ace31): its node, its full-bleed section, and the email underline in the contact section.

### Neutral
- **Canvas Paper** (`#f2f4f7`) page ground with a 22px dot grid on diagram-like regions.
- **Sheet** (`#ffffff`) diagram sheets and client-system boxes.
- **Ink** (`#0c1a2b`) text; **Ink Secondary** (`#3f4f66`) supporting text; **Rule** (`#c9d2de`) hairlines; **Wire** (`#5a6b83`) relationship lines and box borders.

### Named Rules
**The Diagram Legend Rule.** Colour means node type. Navy = person, blue = system, marigold = own product, white = client system. Never use marigold for anything that isn't Lesierse IT's own product or the contact underline.

**The Tinted Secondary Rule.** Secondary text on navy or blue uses `#dce7fb`, never grey (≥5:1 on blue).

## Typography

**Font:** Archivo variable (self-hosted, weight 100–900, width 62–125%), with system sans fallback.

The width axis is the identity: statements run wide (`font-stretch: 112%`), notation runs narrow (`78%`).

### Hierarchy
- **Display** (780, clamp 2.25–3.5rem, wide, -0.025em): hero headline only.
- **Headline** (760, clamp 1.9–2.85rem, wide): section headings, always ending with a full stop.
- **Title** (720–740, 1.25–1.5rem, wide): container and step names.
- **Body** (400, 1.0625rem, 1.6): paragraphs, max ~36rem measure.
- **Notation** (400–650, 0.75–0.8125rem, narrow, +0.02em): type labels in brackets, edge labels, captions, chips, language switch.

### Named Rules
**The Notation Is Not Monospace Rule.** Technical labels use narrowed Archivo, never a monospace costume.

## Layout

Max width 74rem, 24px gutters. Sections breathe at 112px (72px on mobile). Section heads are a two-column grid: headline left, supporting paragraph right, aligned to the baseline. Service containers sit on a 12-column grid in alternating 7/5 and 5/7 spans inside a dashed boundary labelled at its bottom-left corner, as in C4.

Breakpoints: 960px (single column heads and heroes), 760px (nav links hidden, containers stack), 560px (hero diagram becomes a vertical chain).

## Elevation & Depth

Flat diagram language; only the sheets lift off the canvas.

### Shadow Vocabulary
- **sheet** `0 2px 4px rgba(12,26,43,.04), 0 24px 48px -24px rgba(12,26,43,.22)`: hero diagram sheet.
- **button** `0 1px 0 rgba(12,26,43,.25), 0 6px 18px -8px rgba(21,84,209,.7)`: primary button.
- **node-hover** `0 8px 18px -10px rgba(12,26,43,.45)`: linked nodes on hover.

## Shapes

Boxes 6px radius, sheets 10px, boundaries 12px dashed. Person nodes have a 2.25rem rounded top (the C4 person silhouette). Chips 4px. The language switch is the only pill.

## Components

### Buttons
Primary is System Blue, 48px tall, 6px radius, lifts 1px on hover. Quiet is a white sheet with a Rule border that darkens to Wire. On the marigold section the primary turns Ink.

### Chips
Small notation-type tags listing technology inside service containers, 1px border, no fill.

### Cards / Containers
Service containers: 8px radius, generous 32px padding, name + bracketed type + description + chip row pinned to the bottom. No nesting, never icon tiles.

### Navigation
Sticky translucent header with wordmark (blue square glyph, white L, marigold bar), quiet text links and an EN/NL pill switch with the active language filled Ink.

### Diagram Node (signature)
`.node` with `.node-name`, `.node-type`, optional `.node-desc`. Variants: `.node-person`, `.node-core` (system), `.node-own`. A node with `.in` gets a downward arrowhead. Relationships are `.edge` rows containing a non-scaling dashed SVG path and a centred `.edge-label` on a sheet-coloured backing.

**Motion:** the single authored moment is relationships drawing themselves in on load (stroke-dashoffset, 1.1s expo-out, staggered), labels and arrowheads fading in after. Disabled under `prefers-reduced-motion`.

## Do's and Don'ts

### Do:
- **Do** express new content as typed nodes, relationships or boundaries before reaching for generic cards.
- **Do** keep every claim factual; experience is described as skills, never as employer names.
- **Do** keep EN and NL pages structurally identical.

### Don't:
- **Don't** add eyebrow labels above headings; the bracketed type label goes *below* a name.
- **Don't** use gradient text, glass decoration or monospace for "tech" flavour.
- **Don't** invent client logos, testimonials, metrics or prices.
- **Don't** use marigold outside own apps and the contact underline.
