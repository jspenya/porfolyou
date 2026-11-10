---
name: Steph Peña — charcoal & butter
description: A warm, spacious personal home with quiet typography and real work.
colors:
  paper: "#f7f3db"
  ink: "#343530"
  accent: "#62683e"
  muted: "#606151"
  line: "#ceceb7"
  selection: "#dedfb4"
  image-surface: "#fff"
typography:
  display:
    fontFamily: "Lora, Georgia, serif"
    fontSize: "clamp(38px, 4.2vw, 52px)"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "-0.025em"
  headline:
    fontFamily: "Lora, Georgia, serif"
    fontSize: "clamp(30px, 3.2vw, 40px)"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Lora, Georgia, serif"
    fontSize: "clamp(28px, 3vw, 36px)"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "-0.025em"
  body:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.7
rounded:
  control: "4px"
  image: "10px"
spacing:
  gutter: "clamp(24px, 5vw, 64px)"
  section: "clamp(72px, 10vw, 120px)"
  paragraph: "24px"
  letter-paragraph: "26px"
  section-heading: "36px"
  control-gap: "12px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.control}"
    padding: "14px 20px"
  button-primary-hover:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.paper}"
  input:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "14px 16px"
  project-image:
    backgroundColor: "{colors.image-surface}"
    rounded: "{rounded.image}"
  career-row:
    textColor: "{colors.ink}"
    padding: "22px 0"
---

# Design System: Steph Peña

## Overview

**Creative North Star: "A personal letter in charcoal & butter"**

The approved direction is casual, authentic, and laid-back: a personal home whose care is expressed through readable text, warm paper, and generous space. Lowercase headings and an understated serif signature keep it human. The letter metaphor describes the visual voice; it does not prescribe the order of every page section.

This document records the implemented stylesheet and current Jekyll templates. It was extracted manually; the Impeccable engine and its schema/panel validation were unavailable. The approved mockup establishes direction; source values below describe the implementation.

**Key Characteristics:**
- Warm butter paper with charcoal text and restrained olive links.
- Light serif headings paired with clear sans-serif prose.
- One centered reading column with generous vertical rhythm.
- Real project screenshots, subtle rules, and no decorative elevation.

## Colors

### Primary

Olive **accent** identifies links, keyboard focus, and button hover. Charcoal **ink** carries primary text and the solid email action. Preserve the quiet hierarchy rather than spreading the accent across large panels.

### Neutral

Butter **paper** is the continuous page background. **Muted** supplies dates, secondary labels, and helper text. **Line** separates sections and list rows without boxing in prose. **Image-surface** sits behind project screenshots; **selection** highlights selected text.

## Typography

Lora, with Georgia and serif fallbacks, supplies all headings and the name in navigation. DM Sans, with a sans-serif fallback, supplies prose, links, metadata, and controls. There is no monospace role.

The display, headline, and title roles map to h1, h2, and h3. Headings use balanced wrapping. The introduction summary scales from 19px to 22px with `clamp(19px, 2vw, 22px)`. The navigation name is 28px with line height 1.3. Career names use weight 500; other body copy remains 400. Body size drops to 17px on small screens, while metadata stays 15px.

**The Quiet Heading Rule.** Keep headings lowercase and regular weight; establish hierarchy with size and space.

## Layout

Navigation, main content, and footer share a centered maximum width of 980px. Their width is `min(980px, calc(100% - var(--gutter) * 2))`. The fluid gutter and section tokens above preserve breathing room across viewports. No permanent project sidebar is present.

The introduction has fluid top padding (`clamp(48px, 6vw, 72px)`) and 48px below. Prose measures remain bounded: introduction paragraphs at 72ch, case-study text and the personal letter at 70ch, section introductions at 65ch. Standard paragraphs use the paragraph token; letter paragraphs use the slightly looser letter-paragraph token. The personal signoff has 36px above it.

Project screenshots span the content width and have 28px below. Case studies have 56px bottom padding; subsequent projects add a top rule and 48px top padding. Non-work sections use the fluid section space above. Capabilities begin 64px after the career list. Contact has a top rule and 56px top padding. Footer separation uses the section token, followed by 28px top and 40px bottom padding.

At **640px and below**, navigation stacks with left alignment; its links still share one row. The introduction changes to 44px top and 36px bottom padding. Project headings and career rows stack; project image spacing drops to 22px, case-study bottom padding to 40px, and subsequent project top padding to 36px. Capability rows change from `190px 1fr` with a 24px gap to one column with a 4px gap. The email composer stacks. Contact details change from `160px 1fr` with a 20px gap to one column with a 2px gap. The footer stacks with a 16px gap.

**The Breathing Room Rule.** Preserve the section rhythm and bounded prose measures when adding content; do not compress the page into a dense dashboard.

## Elevation & Depth

There are no box shadows, gradients, floating cards, or animated entrances in the implemented system. Depth comes from the continuous paper surface, fine separators, and actual screenshot content. Legacy reveal attributes do not imply an animation.

## Shapes

Fine 1px rules define boundaries. Screenshot frames have the image radius and clip overflow without cropping the natural image aspect ratio. Inputs and the solid email action share the smaller control radius. Text sections remain unboxed.

## Components

### Navigation

An understated serif name anchors the left edge, with three plain text links on the right. Navigation uses charcoal text; hovering underlines a link. A bottom rule closes the header. Desktop padding is 24px vertically; mobile padding is 22px above and 16px below.

### Project frame and heading

A full-width real screenshot sits in a fine bordered frame. Its link opens the original image. The project heading aligns title and metadata on the baseline with a 16px gap; mobile stacks them with an 8px gap. Project titles are rendered lowercase.

### Personal letter

Plain paragraphs, a lowercase greeting, and a simple signoff carry the voice. The quoted verse has rules above and below, 32px vertical margin, and 24px vertical padding. Citation text remains upright, with an ordinary text link.

### Career and capability rows

Career rows use fine bottom rules and a top rule on the first row. Roles appear beneath company names with 4px separation; dates align to the opposite edge on desktop. Hover underlines the company name. Capability rows use 18px vertical padding and restrained secondary labels.

### Contact input and action

The composer has a maximum width of 720px, a 12px gap, and margins of 32px above and 12px below. The input has a muted border, transparent fill, visible label for assistive technology, and olive caret. The charcoal action uses butter text and changes to olive on hover. Submitting opens the visitor's email application; accompanying helper text explains this behavior. No custom error or disabled visual states exist.

### Interaction and accessibility

Links are underlined by default with a 5px underline offset and 1px thickness; hover changes their color to charcoal. All keyboard-focusable elements receive a 2px olive outline with a 5px offset. The skip link becomes visible on focus. Color/background transitions take 160ms with `ease`. Scrolling is smooth with 32px scroll padding; reduced-motion preference disables smooth scrolling and transitions.

## Do's and Don'ts

### Do:
- Do preserve generous spacing and readable prose measures.
- Do use real project screenshots at their natural aspect ratio.
- Do retain visible keyboard focus and reduced-motion behavior.
- Do keep lowercase headings and a casual, personal voice.

### Don't:
- Don't restore the cat identity or permanent project showcase sidebar.
- Don't add shadows or decorative cards to plain prose sections.
- Don't turn the warm, quiet palette into a collection of competing accent colors.
