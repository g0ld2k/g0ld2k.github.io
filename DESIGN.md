---
name: g0ld2k.com
description: Bold app colors, clear typography, and real software.
colors:
  raspberry: "#e21b48"
  yellow: "#ffda16"
  blue: "#0075df"
  ink: "#151518"
  paper: "#ffffff"
  muted: "#56565c"
  line: "#dedee2"
  button-hover: "#f0edf0"
  button-dark-hover: "#3c3c43"
typography:
  display:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "clamp(34px, 3.7vw, 58px)"
    fontWeight: 650
    lineHeight: 1.15
    letterSpacing: "-0.03em"
  app-title:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "clamp(34px, 3.35vw, 52px)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.03em"
  product-title:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "clamp(38px, 4.3vw, 64px)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.03em"
  headline:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "clamp(23px, 2.2vw, 32px)"
    fontWeight: 400
    lineHeight: 1.35
  body:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.6
  prose:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "19px"
    fontWeight: 400
    lineHeight: 1.8
  label:
    fontFamily: '"Encode Sans", sans-serif'
    fontSize: "clamp(17px, 1.35vw, 21px)"
    fontWeight: 600
    lineHeight: 1.35
rounded:
  pill: "999px"
spacing:
  gutter: "clamp(24px, 3vw, 48px)"
  small: "8px"
  control: "12px"
  content: "24px"
  section: "40px"
  major: "72px"
components:
  button-primary:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "12px 26px"
  button-primary-hover:
    backgroundColor: "{colors.button-hover}"
  button-dark:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "12px 26px"
  button-dark-hover:
    backgroundColor: "{colors.button-dark-hover}"
---

# Design System: g0ld2k.com

## Overview

**Creative North Star: "Software Shelf"**

Software Shelf is bold, friendly, and direct: saturated app colors meet a white page, consistent sans-serif typography, and generous space for real product imagery. The independent developer’s identity stays plain and personal.

Flat surfaces and comfortably rounded actions give the work confidence without decorative chrome. The confirmed visual departure is from the previous terminal/neon aesthetic. Existing app screenshots and device compositions carry the product detail; the website does not manufacture interface imagery.

**Key Characteristics:**

- Raspberry, golden yellow, and clear blue app identities.
- Consistent medium-weight titles and readable regular-weight text.
- Flat color regions, white space, and pill-shaped actions.
- Real app imagery with preserved proportions.

## Colors

Saturated, cheerful app accents sit against simple white and near-black neutrals. Frontmatter values come from the implemented stylesheet, not color samples from the approved Mac screenshot.

### Primary

- **Raspberry:** Zoner panels and product hero; also the global caret accent.

### Secondary

- **Golden Yellow:** Contadino panels and product hero.

### Tertiary

- **Clear Blue:** Distance Track panels and product hero.

### Neutral

- **Ink:** primary text on white and yellow, dark actions, and text selection background.
- **Paper:** page backgrounds, light actions, and text on raspberry and blue.
- **Muted Gray:** supporting text on white document and feature surfaces.
- **Fine Gray:** feature and closing-section dividers.
- **Soft White Hover / Charcoal Hover:** light and dark action hover fills respectively.

**The App Identity Rule.** Carry each app’s assigned color from its discovery panel into its product hero; use white text on raspberry and blue, and ink text on yellow.

## Typography

**Display Font:** Encode Sans (sans-serif fallback).
**Body Font:** Encode Sans (sans-serif fallback).

**Character:** A locally hosted variable font supplies the full hierarchy. Titles use restrained weight and tight spacing; ordinary descriptions remain regular weight. There is no separate monospace or decorative display face.

### Hierarchy

- **Display:** the homepage introduction uses the display token, with a smaller responsive override below the shelf breakpoint.
- **App title:** the app-title token is identical across all three panels. Tablet and mobile sizes are documented in Layout.
- **Product title / headline:** product-title identifies the app; the regular-weight headline explains its purpose.
- **Body:** body supplies the default. Product descriptions use (19px / 1.6), capped at (48ch); introductions reach (64ch). Feature descriptions use (18px / 1.65).
- **Prose:** prose supplies long-form documents, with paragraph separation (24px).
- **Label:** label styles the action text. Platform and release labels scale from (16px) to (20px); platform labels use weight (550).

**The Equal Titles Rule.** Give every app name the same type treatment within a shared collection.

## Layout

The layout uses a fluid outer gutter, white navigation, contiguous app regions, and centered reading containers. Product content has a maximum width (1120px); documents use (790px), including their padding. Repeated spacing values in frontmatter are extracted from the CSS, not a newly imposed scale.

The desktop navigation has a minimum height (80px); the homepage introduction has a minimum height (143px). Three equal shelf columns use `minmax(0, 1fr)`. Panels have minimum height `max(680px, calc(100svh - 280px))`, top padding (44px), and bottom padding (30px). Flexible media space aligns platform information and actions. Shelf images use contain fitting and a maximum height (380px); product images use (560px).

Product heroes split copy and media in a (0.85fr / 1.15fr) grid with a (48px) gap. Feature sections use (0.8fr / 1.2fr) columns and a (56px) gap. Major product sections start with (72px) spacing.

Responsive behavior is explicit:

- At (1800px) and wider, shelf panel minimum height is fixed to (744px).
- From (761px) through (1100px), shelf columns remain side by side; titles become (30px), summaries (19px), horizontal panel padding (20px), and actions fill the available width. Platform labels reserve two lines.
- At (900px) and below, product heroes and feature sections become single-column; closing calls to action stack. Product media is capped at (680px) wide, or (440px) for the phone composition.
- At (760px) and below, complete shelf sections stack vertically with (36px 24px) padding and natural height. App titles use `clamp(34px, 8vw, 44px)`; summaries use (21px). The intro title uses `clamp(30px, 7vw, 42px)`. Navigation wraps; product and document top spacing reduces.
- At (410px) and below, navigation links occupy their own full-width row.

## Elevation & Depth

The website has no box shadows. Saturated fields, whitespace, fine dividers, and the depth already present inside real device imagery create separation. App regions are flat and contiguous.

**The Flat Surface Rule.** Use color fields, space, and fine dividers to separate content; the website adds no box shadows.

## Shapes

Page regions and document surfaces have square edges. Actions use the pill radius in frontmatter. Fine dividers use a single-pixel line; screenshots retain their original silhouette and aspect ratio. Inline SVG arrows have rounded strokes.

## Components

### Buttons

Confident, rounded actions pair ink text with paper fill; the closing product action reverses this assignment. Padding and radius are in frontmatter; minimum height is (56px), with an icon gap (10px). Hover changes the fill over (180ms) and moves the forward arrow right (3px) over (200ms), using the shared easing curve in the sidecar. Keyboard focus is a current-color outline (3px) offset by (5px). The implementation has no separate active-state treatment.

### Cards / Containers

App panels are full color sections with square corners and no border or shadow. White reading containers use fine horizontal rules where the content calls for separation. There is no generic floating card component.

### Navigation

The bold wordmark is paired with ordinary text links. Links have a minimum height (44px), underline on hover and current-page state, and share the visible focus outline. Mobile navigation wraps without a menu drawer. The skip link becomes visible on keyboard focus.

### Feature List

A definition list pairs semibold feature names (22px / 1.3) with muted descriptions. Rows separate with fine dividers and (24px) padding and margin; the final row removes its divider and trailing spacing.

### Resource Links

Support and policy links wrap naturally with horizontal gaps (28px) and vertical gaps (8px). Each link has a minimum height (44px). Product pages expose these resources through a hero shortcut and a dedicated resource section.

Motion remains limited to button fill and arrow transitions. Named app links underline immediately on hover; the direction contract’s proposed animated underline extension was not implemented. Reduced-motion preferences disable transitions and animations globally. All content is visible by default.

## Do's and Don'ts

### Do:

- Do preserve the app color assignments and the shared type hierarchy.
- Do show existing app imagery at its natural aspect ratio with contain fitting.
- Do stack complete app sections on narrow screens.
- Do keep support and policy text on readable white document surfaces.
- Do preserve visible keyboard focus and reduced-motion behavior.

### Don't:

- Don’t revive the previous terminal/neon ornaments.
- Don’t fabricate app screenshots or replace interface details with generated imagery.
- Don’t turn the mobile app collection into a horizontal carousel.
- Don’t add raised card chrome to the contiguous app panels.
