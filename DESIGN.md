---
name: Ricardo Fragoso
description: Personal trainer one-pager — measured, ruled, unhurried; moss-dark and sand with sparing mustard.
colors:
  moss-dark: "#141A16"
  moss-dark-2: "#1B221D"
  moss-dark-3: "#232B25"
  sand: "#F2EFE6"
  sand-2: "#E8E4D8"
  olive: "#8A9A6E"
  olive-deep: "#4E5A3B"
  mustard: "#D8C27A"
  mustard-hi: "#E4D08F"
  text-light: "#EDEBE4"
  muted-light: "#A9B0A2"
  text-dark: "#1B221D"
  muted-dark: "#4F584F"
  placeholder-dark: "#3A453C"
  placeholder-sand: "#CDD1C3"
typography:
  display:
    fontFamily: "Oswald, Arial Narrow, sans-serif"
    fontSize: "clamp(2.6rem, 5.4vw, 4.75rem)"
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: "-0.01em"
  h2:
    fontFamily: "Oswald, Arial Narrow, sans-serif"
    fontSize: "clamp(2.25rem, 5.2vw, 3.75rem)"
    fontWeight: 500
    lineHeight: 1.05
  display-light:
    fontFamily: "Oswald, Arial Narrow, sans-serif"
    fontSize: "clamp(1.9rem, 4.2vw, 3.25rem)"
    fontWeight: 300
    lineHeight: 1.15
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.65
rounded:
  sm: "8px"
  md: "12px"
  pill: "999px"
spacing:
  gutter: "clamp(1rem, 4vw, 2.5rem)"
  section-y: "clamp(5rem, 11vw, 9rem)"
components:
  button-primary:
    backgroundColor: "{colors.mustard}"
    textColor: "{colors.moss-dark}"
    rounded: "{rounded.sm}"
    padding: "14px 26px"
    height: "52px"
  button-primary-hover:
    backgroundColor: "{colors.mustard-hi}"
  button-dark:
    backgroundColor: "{colors.text-dark}"
    textColor: "{colors.sand}"
    rounded: "{rounded.sm}"
    height: "52px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.text-light}"
    rounded: "{rounded.sm}"
    height: "52px"
  plan-card:
    backgroundColor: "{colors.moss-dark-2}"
    rounded: "{rounded.md}"
    padding: "40px"
  plan-card-featured:
    backgroundColor: "{colors.moss-dark-3}"
---

# Design System: Ricardo Fragoso

## Overview
A trainer's page that reads like a well-made training plan: measured, ruled, unhurried. Near-black moss sections alternate with sand sections for rhythm; large condensed uppercase Oswald headlines carry authority; 1px hairlines and generous whitespace do the structuring instead of boxes. Masculine, sober, never neon or "gym poster".

## Colors
### Primary
Mustard `#D8C27A` — the only call-to-action color on dark grounds, plus numerals (stats, pillar numbers) and the hero's second line. Use sparingly: if more than one mustard element competes per viewport besides the floating button, remove one.
### Secondary
Olive/sage `#8A9A6E` — icons, rules, tags, the final CTA field. On sand, use `olive-deep #4E5A3B` for text (AA contrast).
### Neutral
Moss dark `#141A16` (page), `#1B221D` / `#232B25` (cards, raised); sand `#F2EFE6` (alternating sections). Text light `#EDEBE4`, muted `#A9B0A2`; text dark `#1B221D`, muted `#4F584F`.
### Named Rules
- **The Alternation Rule:** sections alternate dark → sand → dark; never two sand sections touching.
- **No pink, no neon:** warm-feminine and glowing accents are outside the world.

## Typography
Oswald (300/500) for display, uppercase for H1–H3; weight 300 sentence case for quotes and subtitles. Inter for body and UI.
### Hierarchy
H1 up to 4.75rem · H2 up to 3.75rem · H3 1.3–2.1rem uppercase · body 1.0625rem/1.65 · small labels 0.75–0.85rem uppercase tracked only inside tags/pills.

## Layout
Max width 1180px, fluid gutter, section padding clamp(5rem, 11vw, 9rem). Two-column hero/about collapse to one column at 860px; grids of 3–4 collapse to 1 on phones; testimonials become a scroll-snap carousel ≤860px.

## Elevation & Depth
Mostly flat. Soft offset shadows only on primary-button hover, the featured plan and the floating WhatsApp button. Depth also from a fine offset hairline frame behind the hero portrait.

## Shapes
Radius 8px (buttons, small surfaces), 12px (cards, photo frames), pills for tags. 1px hairlines (`rgba(237,235,228,.12)` on dark, `rgba(27,34,29,.14)` on sand).

## Components
### Buttons
Primary mustard on dark; `btn-dark` (moss on sand); ghost outline. Min height 52px, Inter 600. Every WhatsApp button carries the WhatsApp glyph and a prefilled message via `data-wa`.
### Chips
Uppercase pill tags on plan cards and testimonial goals; the featured plan's tag is solid mustard.
### Cards / Containers
Plan cards: moss-dark-2 with hairline border; featured = mustard border. Testimonials: near-white card on sand. Method pillars are ruled columns, not boxed cards.
### Navigation
Fixed 72px bar, transparent over hero, blurred moss once scrolled; underline-on-hover in mustard; hamburger + full-screen drawer ≤960px.
### Photo placeholder
Grey-green block, 1px dashed border, centered uppercase Oswald label "FOTO DO RICARDO – …", camera glyph top-left, fixed aspect ratio (4:5, 3:4, 1:1). Replace with `<img class="photo ph-4x5">`.

## Do's and Don'ts
### Do:
- Keep one primary action per block, always WhatsApp.
- Let hairlines and whitespace separate content.
### Don't:
- Don't add eyebrow labels above section headings.
- Don't use gradient text, glows or more than one accent color per element.
