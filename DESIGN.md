---
name: Higgins Hardwood Flooring
description: Calm navy-and-gold bands from the owner's logo, one free-estimate ask, phone first.
colors:
  paper: "#f6f5f1"
  card: "#ffffff"
  field: "#e3e5ee"
  ink: "#0f132e"
  body: "#2b2f45"
  soft: "#4b5068"
  navy: "#1b2352"
  deep: "#0f132e"
  on-dark: "#f6f5f1"
  on-dark-soft: "#c6cbe0"
  gold: "#c9a24a"
  gold-2: "#d8b665"
  gold-ink: "#7a5a12"
  focus: "#33449a"
  error: "#b3261e"
typography:
  display:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(42px, 12vw, 80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-0.005em"
  headline:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(30px, 7.6vw, 48px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.005em"
  title:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(24px, 6.4vw, 30px)"
    fontWeight: 400
    lineHeight: 1.15
  ui:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.2
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(18px, 4.8vw, 20px)"
    fontWeight: 400
    lineHeight: 1.5
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "14px"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: "0.02em"
rounded:
  field: "10px"
  panel: "20px"
  card: "24px"
  pill: "999px"
spacing:
  gutter-phone: "20px"
  gutter-desktop: "40px"
  section-phone: "64px"
  section-desktop: "96px"
  column-gap: "64px"
  container: "1160px"
components:
  button-primary:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.ink}"
    typography: "{typography.ui}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.gold-2}"
    textColor: "{colors.ink}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.ui}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  input:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  chip:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "48px"
  chip-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.card}"
  form-card:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.card}"
    padding: "clamp(20px, 5vw, 32px)"
  eyebrow:
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "9px 14px"
  float-contact:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.ink}"
    size: "60px"
---

# Design System: Higgins Hardwood Flooring

## Overview

**Creative North Star: "The Logo, Laid Out as a Floor"**

Ellie's calm band style applied to one floor man's logo. The page is a stack of full-width bands: warm paper, the logo's mid navy, the logo's deep navy with a faint diagonal line texture. Gold appears as the logo uses it, as a solid fill (buttons, step numbers, the contact circle) and never as text on light. Headings are Cal Sans at weight 400; everything else is the system face. Density is low: one idea per band, generous section padding, large tap targets.

Motion is limited to three moves: the hero H1 letter bounce-in, one 12px fade-up for content that starts below the first screen, and the floating contact circle sliding up. Nothing else animates.

The hero photo and the finish photo are **generated examples** (gpt-image-1), not the owner's jobs. Swap them for real work photos as soon as he sends any; keep the navy shade over the hero so the white H1 still reads.

Contact is **Messenger only** until `CONFIG.PHONE` is set in the script. Setting it switches the header link, closing link, form button and floating circle to call or text, and swaps their icons. Don't hard-code a phone link anywhere in the markup.

**Key Characteristics:**
- Full-bleed bands in a fixed rotation: hero (deep + photo), navy, paper, deep, paper, navy, deep footer.
- Gold is a fill. Gold as text appears only on dark bands; on light it becomes gold-ink.
- Pills for actions and chips, 24px cards for containers, circles for arrows, step numbers and the contact button.
- Every action leads to the one estimate form or Messenger.

## Colors

Two navies and a gold taken from the logo, over off-white paper.

### Primary
- **Logo Gold** (gold): fill only. Primary buttons, step-number discs, the floating contact circle, the eyebrow dot, arrow discs on hover, text selection. Text on it is always ink.
- **Pale Gold** (gold-2): hover state of the primary button only.
- **Gold Ink** (gold-ink): gold when it has to be text or an icon on a light ground (the header Messenger icon and hover). 5.8:1 on paper.

### Secondary
- **Logo Navy** (navy): the services band and the closing band.
- **Deep Navy** (deep): hero base and shade, the How it works band and the footer, both carrying the line texture. Same value as ink.

### Neutral
- **Paper** (paper): page ground, header, the care and estimate bands. Also the browser theme colour.
- **Card White** (card): the form card and the Facebook card.
- **Field Mist** (field): inputs and unselected chips on the white form.
- **Ink** (ink): headings and labels on light, text on gold, the selected chip fill.
- **Body Slate** (body): running text on light.
- **Soft Slate** (soft): ledes, placeholders, helper text on light.
- **On-Dark** (on-dark) and **On-Dark Soft** (on-dark-soft): headings and running text on navy and deep bands.
- **Focus Blue** (focus): focus and hover outlines on light grounds. On dark bands the focus outline turns gold.
- **Error Red** (error): field error border and message.
- Hairlines are ink or white at low alpha (`rgba(15,19,46,.12)` on light, `rgba(255,255,255,.12)` between service rows on navy).

### Named Rules
**The Gold Is a Fill Rule.** Never set text in gold on paper or white. Use gold-ink for text on light, and gold text only on navy, deep or the shaded hero.

**The Accent Phrase Rule.** On dark bands the heading's last word or phrase is gold ("Philly.", "do.", "works."). Light-band headings stay all ink.

**The Two Focus Colours Rule.** Focus outlines are 3px with a 3px offset: focus blue on light grounds, gold on navy, deep, hero and footer.

## Typography

**Display Font:** Cal Sans 400 (fallback Avenir Next, Segoe UI, system-ui)
**Body Font:** system stack (-apple-system, Segoe UI, Helvetica Neue, Arial)

**Character:** A rounded geometric display face for every heading and every tappable label, with the phone's own font for reading text. That keeps it friendly and quick to load in Facebook's in-app browser.

### Hierarchy
- **Display** (hero H1 only): white, max 12ch, balanced wrap. Drops to `clamp(36px, 9vh, 56px)` on landscape phones.
- **Headline** (section H2s): ink on light, on-dark on dark bands.
- **Title** (service rows, 24px step titles, the closing "Message me" link at `clamp(28px, 8vw, 44px)`).
- **UI** (Cal Sans 18px, 20px for the header link on desktop): buttons, form labels and legends, header brand name, Facebook card label, step numbers.
- **Lede** (`clamp(18px, 4.8vw, 20px)`): hero promise, section intros, closing area line; max 32 to 40ch.
- **Body** (16px/1.7): running text, inputs, chips, footer.
- **Label** (14px): eyebrow pills (500, 0.02em), "(optional)" hints and the line under the submit button.

### Named Rules
**The Cal Sans Means Tap or Heading Rule.** Cal Sans is for headings and things you press or label. Paragraphs are never in Cal Sans.

**The Four UI Tiers Rule.** Non-heading sizes are 14, 16, 18 and 20px. Don't add a fifth.

## Layout

Single column on phones. Container max width 1160px with 20px gutters, rising to 40px at 760px. Sections pad 64px top and bottom, rising to 96px at 760px. At 760px the hero gets more top and bottom room and its buttons sit side by side (min 260px each). At 1024px: service rows split into two columns (64px gap), the care band becomes photo-right / text-left, the estimate band becomes intro-left (sticky at 40px) / form-right, the steps become three columns, and the closing band becomes logo / text / link in a row. Tap targets are at least 44px; buttons are 56px tall and full width inside the form.

## Elevation & Depth

Flat. Depth comes from band colour changes, the white form card on paper, and the navy shade over the hero photo (top to bottom on phones, left to right on desktop). Only the floating contact circle has a shadow.

### Shadow Vocabulary
- **Float lift** (`box-shadow: 0 10px 28px rgba(15,19,46,.3)`): the floating contact circle only.

### Named Rules
**The One Shadow Rule.** The contact circle is the only element with a shadow. Cards, buttons and chips stay flat, with no hover shadow.

## Shapes

Four radii: pill (999px) for buttons, chips and eyebrows; 24px for the form card and the care photo; 20px for the Facebook card and the closing logo; 10px for inputs and the header mark. Arrows, step numbers and the contact circle are full circles (44px, 48px, 60px). Borders are 2px and transparent at rest, so hover and focus colour them without shifting the layout.

## Components

### Buttons
- **Shape:** pill, 56px tall, 26px side padding, Cal Sans 18px, optional 20px leading icon.
- **Primary:** gold fill, ink text. Hover (pointer devices only) is pale gold. Press scales to 0.98.
- **Line:** transparent with a 2px ink border. Hover is a 6% ink wash. Used only for the secondary Copy action.
- **In the form:** full width. Hover adds a 3px focus-blue outline.
- At most two buttons in a group: one primary, one line.

### Chips
- **Style:** field-mist pill, 48px tall, 2px transparent border, 16px system text. The radio input is visually hidden.
- **State:** hover gives a focus-blue border. Selected is an ink fill with white text.

### Cards / Containers
- **Form card:** white, 24px corners, padding `clamp(20px, 5vw, 32px)`, 20px gap between fields, max 600px.
- **Facebook card:** white, 20px corners, min 72px tall, label left and arrow disc right, max 440px.
- **Photo frame:** 24px corners, 4:5 ratio, max 420px tall (560px on desktop), warm tan placeholder `#d9c6a0` while loading.

### Inputs / Fields
- **Style:** field-mist fill, 2px transparent border, 10px corners, 52px min height (textarea 110px), ink text, soft placeholder. Labels are Cal Sans 18px in ink.
- **Focus:** the border turns focus blue (and on hover too).
- **Error:** the border and a 16px message turn error red. The message clears as soon as the field gets a value.

### Navigation
- **Header:** paper, 68px tall (80px on desktop). Logo mark plus Cal Sans name on the left, Cal Sans "Message me" with a gold-ink icon on the right. No menu.
- **Footer:** deep navy with line texture, on-dark links at 44px tap height that turn gold on hover. Extra bottom padding clears the floating circle.

### Service Rows (signature)
Each service is a full-width link on navy, Cal Sans title size, 76px min height, with white hairlines between rows and a 44px translucent arrow disc on the right that turns gold on hover or focus. Tapping a row pre-selects the matching chip in the form.

### Step Numbers (signature)
A 48px gold disc with an ink Cal Sans numeral, sitting beside a 24px Cal Sans title and a body line.

### Eyebrow Pill (Ellie's house-style exception)
A quiet 14px label pill with a 7px gold dot: ink on a 6% ink wash on light, on-dark on a 12% white wash on dark. Used twice only: above the hero H1 and above the estimate heading, and each one carries a real fact (the offer, the service area). It never has an arrow, hover, shadow or solid gold fill, and it is never marked up as a heading. Impeccable's craft floor flags eyebrows. This one is Ellie's documented choice, so treat it as a limited exception and not a label for every section.

### Floating Contact Circle (signature)
A 60px gold circle with an ink chat icon, fixed bottom right inside the safe area, using the float-lift shadow. It slides up (0.35s, `cubic-bezier(.2,.8,.2,1)`) once the hero has scrolled away, and hides while the form or the closing link is on screen. It is one circle, never a bottom bar. `CONFIG.FLOAT = false` removes it.

### Hero H1 Bounce-in (signature motion)
Each letter slides in from 50px to the right with a slight overshoot (1s, `cubic-bezier(.34,1.56,.64,1)`, 20ms apart). It waits up to 800ms for Cal Sans, then puts the plain heading back so kerning and selection return. JS only; skipped under reduced motion.

### Fade-up
Anything with the rise class that starts below the first screen fades in and rises 12px (0.4s ease-out). Content is visible at rest, and reduced motion turns it off.

## Do's and Don'ts

### Do:
- **Do** use the colour tokens in `:root` for any new colour. Gold-ink is the only gold for text on light.
- **Do** keep the band rotation: a light band between each pair of dark ones.
- **Do** put the last word of a dark-band heading in the accent span.
- **Do** keep hover styles inside `@media (hover:hover)` so taps don't leave them stuck on.
- **Do** keep 44px minimum tap targets and the 56px button height.
- **Do** replace the generated hero and finish photos with the owner's real work when it arrives, keeping the navy shade.
- **Do** switch contact by setting `CONFIG.PHONE` / `CONFIG.PHONE_SHOWN`, not by editing links.

### Don't:
- **Don't** set gold text on paper or white, or put white text on gold.
- **Don't** add shadows to cards, buttons or chips; the contact circle is the only lifted element.
- **Don't** add new motion beyond the H1 bounce-in, the one 12px fade-up and the circle slide.
- **Don't** add eyebrows above more headings, or give one an arrow, hover or gold fill.
- **Don't** turn the floating circle into a bottom bar or add a second floating button.
- **Don't** add a Call button to the hero; the number goes in the header's top-right once it exists.
- **Don't** set paragraphs in Cal Sans or add a size outside the 14/16/18/20 UI tiers.
