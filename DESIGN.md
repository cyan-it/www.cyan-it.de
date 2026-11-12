---
name: Cyan IT
description: A print-separation proof sheet. Process cyan laid over a black keyline plate on cool paper.
colors:
  paper: "#f7f9fa"
  ink: "#0c1a22"
  mute: "#4a5b66"
  process-cyan: "#008acb"
  deep-cyan: "#00608f"
  plate-black: "#021018"
  keyline: "rgb(12 26 34 / 0.22)"
typography:
  display:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.75rem, 9.2vw, 6rem)"
    fontWeight: 850
    lineHeight: 0.98
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(1.9rem, 4.4vw, 3.25rem)"
    fontWeight: 800
    lineHeight: 1.05
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(1.25rem, 2.2vw, 1.6rem)"
    fontWeight: 720
    lineHeight: 1.2
  body:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Archivo, Helvetica Neue, Arial, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 560
    lineHeight: 1.6
rounded:
  none: "0"
spacing:
  pad: "clamp(1.25rem, 4vw, 3.5rem)"
  gutter: "1.5rem"
  section: "clamp(2.5rem, 6vw, 5rem)"
components:
  button-primary:
    backgroundColor: "{colors.deep-cyan}"
    textColor: "#ffffff"
    rounded: "{rounded.none}"
    padding: "0.9rem 1.4rem"
  button-primary-hover:
    backgroundColor: "{colors.ink}"
    textColor: "#ffffff"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.deep-cyan}"
    rounded: "{rounded.none}"
    padding: "0.9rem 1.4rem"
  button-secondary-hover:
    backgroundColor: "{colors.deep-cyan}"
    textColor: "#ffffff"
  button-on-field:
    backgroundColor: "#ffffff"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "0.9rem 1.4rem"
---

# Design System: Cyan IT

## Scope and status

Only `src/index.html` (styled by `src/assets/css/home.css`) uses this system. The roughly 50 inner pages still ship the old Squarespace CSS and do not match what is written here. The closing band is a known partial: it is a flat deep-cyan field with white crop marks and a registration target, with no overprint (multiply) interaction yet.

## Overview

**Creative North Star: "The Proof Sheet"**

The homepage reads as a print-separation proof. Process cyan is one ink laid over a black keyline plate on cool paper. The two plates are visibly separate: the headline fills in cyan while its black outline slides into register on load. Furniture from the press room (crop marks, registration targets, a 10 to 100 percent tint ramp) does the work that icons, cards and banners do on a template page.

Density is calm and editorial. Hairline ink rules divide sections; columns sit on a 12-column grid; the case studies come before the pitch. Archivo's width and weight axes carry all hierarchy, so there is one family and no ornament.

**Key Characteristics:**
- One family, two axes: Archivo variable, weight 400 to 850, width 96% to 110%.
- Cyan is ink, not decoration: fill for large display, deeper cyan for text and fields.
- Flat and square: no radius, no shadow, no gradient, no cards.
- Print furniture (crop marks, targets, tint ramp) replaces icons and containers.
- Hairlines in ink or 22% ink, never boxes.

## Colors

A cool paper ground, near-black ink, and a single cyan in two strengths.

### Primary
- **Process Cyan** (#008acb): the fill ink. Large display fill (the h1 plate), tint-ramp swatches, offer tint bars, scrollbar and selection. Contrast on paper is about 3.6:1, so it is never used for body-size text.
- **Deep Cyan** (#00608f): the text and field ink. Links, primary button, focus ring, current-nav state, and the closing band field (white text on it is high contrast).

### Neutral
- **Cool Paper** (#f7f9fa): page ground and dropdown/menu surfaces.
- **Ink** (#0c1a22): body text, section top rules, keylines, crop marks, hover state of buttons.
- **Mute Slate** (#4a5b66): captions, figcaptions, ramp labels.
- **Plate Black** (#021018): backing behind raster plates while they load; matches the dark crane and case images.
- **Keyline** (rgb 12 26 34 at 22%): soft dividers between cases and offers.

### Named Rules
**The Two-Plate Rule.** Cyan fills, ink outlines. Large cyan shapes sit over or beside an ink keyline; cyan alone never carries small text.

**The Overprint Rule.** Where cyan or a tint meets paper or an image, it is laid with `mix-blend-mode: multiply` so the layers read as ink, not as opaque paint. (The closing band does not do this yet; see Scope.)

## Typography

**Display, Headline, Body, Label Font:** Archivo variable (self-hosted `archivo-latin-wdth.woff2`, weight 100 to 900, width 62% to 125%), falling back to Helvetica Neue, Arial, sans-serif.

**Character:** Wide, heavy and tight at display size; narrower and lighter for reading. Width is used as a second voice: UI labels run at 106 to 110%, quotes and leads at 96%.

### Hierarchy
- **Display** (850, clamp 2.75rem to 6rem, 0.98, -0.025em, width 104%): the h1 only, in two stacked plates (cyan fill, ink outline).
- **Headline** (800, clamp 1.9rem to 3.25rem, 1.05, -0.02em, width 104%, balanced wrap): section h2.
- **Title** (720, clamp 1.25rem to 1.6rem, 1.2, width 104%): case and offer h3.
- **Body** (400, 1.0625rem, 1.6): paragraphs capped at 62ch.
- **Lead** (clamp 1.2rem to 1.6rem, 1.4, width 96%, 30ch): the single hero sentence. The "big" statement in the Cyantists section is clamp 1.35rem to 2.1rem, 1.3, 26ch.
- **Label** (560, 0.95rem, width 108%): navigation. Buttons use 620 at width 108%; inline "more" links use 600 at 104%.
- **Caption** (0.85 to 0.88rem, Mute Slate): figcaptions and quote attribution.

### Named Rules
**The One Family Rule.** Hierarchy comes from weight and width on Archivo. A second typeface is not introduced.

**The Tabular Rule.** Numeric furniture (tint-ramp labels, address block) uses tabular numerals.

## Layout

A centered `.wrap` (max 84rem) with fluid side padding (1.25rem to 3.5rem) hosts a 12-column grid with a 1.5rem gutter. Hero: copy on columns 1 to 8, image plate on 9 to 12, bottom-aligned. Text sections use a 5/6 split (h2 on 1 to 5, copy on 7 to 12). Case rows put a 3-column plate left and a 9-column body right, which splits into text (5) and quote (4). Offers are three equal columns divided by keylines. Sections are separated by a 1px ink top rule; vertical rhythm uses clamp 2.5rem to 5rem.

Below 56rem everything collapses to one column; the hero plate is capped at 22rem, case plates at 14rem, and navigation becomes a Menü button with a stacked panel (only when JS is present). Section padding, gutters, and plate sizes are the only spacing values reused; there is no spacing scale beyond these.

## Elevation & Depth

Flat. There are no shadows and no gradients (the crop-mark lines are hairline gradient strokes, not surfaces). Depth comes from overlap and overprint: the sticker overlaps the hero plate corner, the keyline plate offsets the cyan plate by a few tenths of a rem, and multiply blending lets tints stack like ink.

### Named Rules
**The Flat-Proof Rule.** Nothing floats. A hover may rotate or recolor an element, never lift it with a shadow.

## Shapes

Square corners everywhere (radius 0). Borders are 1px hairlines in ink or Keyline. Image plates are portrait crops (800:875) with eight L-shaped crop marks (0.8rem arms, 1px, inset -0.9rem) drawn around them. A registration target (1.6rem circle with crosshair, 1px stroke) marks the hero plate and the closing band. The tab of a section (a 3.5rem by 0.5rem bar) appears as a keyline rectangle with a cyan multiplied copy offset by 0.4rem and 0.3rem.

## Components

### Buttons
- **Shape:** square, 1px border in the fill colour, padding 0.9rem 1.4rem, weight 620, width 108%.
- **Primary:** Deep Cyan fill, white text. Hover goes to Ink fill and border.
- **Secondary:** transparent, Deep Cyan text and border. Hover fills Deep Cyan with white text.
- **On field (closing band):** white fill, Ink text. Hover goes to Ink with white text.
- **Transition:** background and colour in 0.2s; disabled under reduced motion.

### Navigation
Archivo 560 at 108% and 0.95rem in Ink, no underline at rest. Hover and current page: Deep Cyan with an underline offset 0.35em. The Leistungen item is a native `details` dropdown: a paper panel with a 1px ink border, 17rem wide, and a CSS chevron on the summary. Focus is a 3px Deep Cyan outline offset 3px.

### Image plate
A figure with crop marks around it, portrait crop on a Plate Black backing. On the hero plate, the registration target sits above the top-right corner and the hiring sticker overlaps the lower-left (hover rotates it -6 degrees and scales 1.04).

### Case row
Plate left, then title and copy, with a quote block at its right that begins with a 1px ink rule. Quote text is 1.15rem at weight 420, attribution in Mute Slate, client logos multiplied onto paper. Rows are separated by Keyline hairlines.

### Offer column
Three columns under an ink rule. Each has a short multiplied cyan bar above it whose tint steps down across columns (100%, 62%, 30%), echoing the ramp. The title is an ink link that turns Deep Cyan on hover.

### Tint ramp
Ten swatches of Process Cyan mixed into paper at 10 to 100 percent, with percentage labels below. Decorative (aria-hidden), shown under the hero fold and again as the footer bar, and hidden in print.

### Closing band
Full-bleed Deep Cyan field with white text, white crop marks inset from the wrapper and a white registration target. This is a flat partial (see Scope).

## Do's and Don'ts

### Do:
- **Do** use Process Cyan (#008acb) only for large fills and tints; use Deep Cyan (#00608f) for text, links and buttons.
- **Do** build hierarchy with Archivo weight and width alone.
- **Do** separate sections with a 1px Ink rule and groups with Keyline hairlines.
- **Do** frame photographic plates with the eight crop marks and a Plate Black backing.
- **Do** lay tints and logos with multiply so they overprint the paper.
- **Do** keep the 3px Deep Cyan focus outline (white on the closing band) and honour reduced motion.

### Don't:
- **Don't** use shadows, gradients as surfaces, rounded corners, or card containers; the world has none of them.
- **Don't** set body-size text in Process Cyan.
- **Don't** add a second typeface or an icon set; the print furniture is the only ornament.
- **Don't** apply this system to the inner Squarespace pages by patching; they are unconverted and remain a separate migration.
