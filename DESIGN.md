---
name: Shoot
description: Hyper-local café ordering – the café carries your coffee to the spot where you already are.
colors:
  roasted-rust: "#AE431E"
  caramel-orange: "#D06224"
  olive-leaf: "#8A8635"
  oat-sand: "#E9C891"
  steamed-milk: "#F1E3C6"
  espresso-brown: "#4A2C1E"
  porcelain-white: "#FFFFFF"
  espresso-soft: "#6B5040"
  espresso-faint: "#7A604F"
  espresso-raised: "#5E3D2C"
  milk-foam-dim: "#C9B49A"
typography:
  display:
    fontFamily: "Shrikhand, Georgia, serif"
    fontSize: "34px"
    fontWeight: 400
    lineHeight: 1.12
    letterSpacing: "0em"
  headline-large:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "34px"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "28px"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "-0.015em"
  title:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "22px"
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.45
  button:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "17px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.005em"
  subhead:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.4
  label:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: "0.06em"
  caption:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "13px"
    fontWeight: 500
    lineHeight: 1.35
  micro:
    fontFamily: "Inter, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "12px"
    fontWeight: 500
    lineHeight: 1.2
rounded:
  xs: "6px"
  sm: "8px"
  thumb: "14px"
  input: "16px"
  card: "20px"
  frame: "24px"
  sheet: "28px"
  pill: "999px"
spacing:
  "1": "4px"
  "2": "8px"
  "3": "12px"
  "4": "16px"
  "5": "20px"
  "6": "24px"
  "8": "32px"
  "10": "40px"
  "12": "48px"
  gutter: "24px"
components:
  button-primary:
    backgroundColor: "{colors.roasted-rust}"
    textColor: "{colors.porcelain-white}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 24px"
    height: "56px"
  button-primary-pressed:
    backgroundColor: "#9C3F1E"
    textColor: "{colors.porcelain-white}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.espresso-brown}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 24px"
    height: "56px"
  button-disabled:
    backgroundColor: "{colors.oat-sand}"
    textColor: "{colors.espresso-soft}"
  button-camera:
    backgroundColor: "{colors.steamed-milk}"
    textColor: "{colors.espresso-brown}"
    rounded: "{rounded.pill}"
    height: "56px"
  button-system:
    backgroundColor: "{colors.espresso-brown}"
    textColor: "{colors.steamed-milk}"
    rounded: "{rounded.pill}"
    height: "56px"
  chip:
    backgroundColor: "{colors.porcelain-white}"
    textColor: "{colors.espresso-brown}"
    typography: "{typography.subhead}"
    rounded: "{rounded.pill}"
    padding: "0 16px"
    height: "44px"
  chip-selected:
    backgroundColor: "{colors.espresso-brown}"
    textColor: "{colors.steamed-milk}"
  badge:
    backgroundColor: "{colors.oat-sand}"
    textColor: "{colors.espresso-brown}"
    typography: "{typography.caption}"
    rounded: "{rounded.pill}"
    padding: "0 12px"
    height: "28px"
  input:
    backgroundColor: "{colors.porcelain-white}"
    textColor: "{colors.espresso-brown}"
    typography: "{typography.body}"
    rounded: "{rounded.input}"
    padding: "0 16px"
    height: "56px"
  card:
    backgroundColor: "{colors.porcelain-white}"
    textColor: "{colors.espresso-brown}"
    rounded: "{rounded.card}"
    padding: "12px 16px 12px 12px"
  info-box:
    backgroundColor: "{colors.oat-sand}"
    textColor: "{colors.espresso-brown}"
    rounded: "{rounded.input}"
    padding: "14px 16px"
  sheet:
    backgroundColor: "{colors.porcelain-white}"
    textColor: "{colors.espresso-brown}"
    rounded: "{rounded.sheet}"
    padding: "10px 20px 34px"
  tab-active:
    backgroundColor: "{colors.caramel-orange}"
    textColor: "{colors.porcelain-white}"
    rounded: "{rounded.pill}"
    width: "60px"
    height: "32px"
  bubble-in:
    backgroundColor: "{colors.porcelain-white}"
    textColor: "{colors.espresso-brown}"
    rounded: "20px"
    padding: "10px 16px"
  bubble-out:
    backgroundColor: "{colors.espresso-brown}"
    textColor: "{colors.steamed-milk}"
    rounded: "20px"
    padding: "10px 16px"
---

# Design System: Shoot

> Source of every value: `design-system/tokens.css` (single source of truth) and `design-system/components.css`. Living reference: `design-system/index.html`. This file describes them; if the two ever disagree, the CSS wins and this file is stale.

## Overview

**Creative North Star: "The Hand-Carried Cup"**

Shoot exists because a person from the café walks over with your coffee. Nothing in the interface is allowed to feel like a platform standing between that café and you. The UI is the tray the cup is carried on: warm, steady, quiet, and gone from attention the moment the order is placed. Its warmth comes from café materials, not decoration: steamed-milk cream for the ground, espresso brown for every word and icon, a roasted-rust button you press once per screen.

The mood is **warm, friendly and calm**. Screens follow the Starbucks-calm brief: plenty of cream around one clear action, the primary button docked low in thumb reach, short copy. Personality lives in a few deliberate places only: the Shrikhand wordmark and a handful of short headlines, the one-colour illustrations, the caramel-orange accents that mark "now" (the active tab, the ETA progress, your pin on the map). Everything you read twice, prices, times, buttons, labels, is plain Inter.

The interface is used outdoors, in sunlight, with one hand, for a few seconds at a time. That is why contrast is high, tap targets are never under 44 px, and states are always carried by an icon and words, never by colour alone.

**Key Characteristics:**
- Cream ground, espresso-brown ink, white cards lifted by soft brown-tinted shadows.
- One roasted-rust pill button per screen, docked at the bottom.
- Caramel orange marks what is live or selected; olive marks "in range / done"; neither ever carries small text.
- Shrikhand is a garnish (wordmark + four short headlines); Inter does all the work.
- Camera screens flip to an espresso-brown ground with cream text, never black.
- Pill buttons and chips, 20 px cards, 28 px sheets with a grabber.

## Colors

A café palette: roasted coffee, caramel, olive leaf, oat and steamed milk, with espresso as the only dark.

### Primary
- **Roasted Rust** (#AE431E): primary action buttons (white text, 5.80:1), text links, the send button, error outlines and error icon circles. The one colour that means "do this".

### Secondary
- **Caramel Orange** (#D06224): the brand accent. Wordmark, active tab pill, done segments of the order progress, your pin on maps, warning icons and outlines, focus ring. Fails AA for small text, so it only carries icons, shapes and display text of 24 px or more.

### Tertiary
- **Olive Leaf** (#8A8635): "in range", "delivered", "done". Check circles, the in-range ring, live dots, delivery radius on maps. Never text: always an icon beside a brown label.

### Neutral
- **Steamed Milk** (#F1E3C6): the app background on every light screen; the text colour on brown (9.91:1).
- **Porcelain White** (#FFFFFF): cards, sheets, inputs and the tab bar lifted off the cream.
- **Oat Sand** (#E9C891): secondary surfaces. Info and privacy boxes, neutral badges, empty progress segments, disabled buttons, illustration fills, avatar backgrounds.
- **Espresso Brown** (#4A2C1E): all text and icons, secondary button outlines, outgoing chat bubbles, the camera-screen ground.
- **Espresso Soft** (#6B5040): secondary text (5.81:1 on cream, 4.61:1 on sand). Replaces grey everywhere.
- **Espresso Faint** (#7A604F): input placeholders on white.
- **Espresso Raised** (#5E3D2C): raised surfaces on camera screens (the viewfinder before the image loads).
- **Milk Foam Dim** (#C9B49A): secondary text on camera screens (6.27:1 on brown).

Hairlines and outlines are espresso at low alpha (14% hairline, 32% outline); scrims are espresso at 42%. Map land, roads and parks are mixed from sand, cream, white and olive.

### Named Rules
**The No-Grey Rule.** There is no grey in Shoot. Secondary text, borders, scrims and shadows are all espresso brown at reduced strength.

**The One Rust Rule.** Each screen has exactly one roasted-rust button. Everything else is a brown outline, a text link or a chip.

**The Accent-Is-Not-Text Rule.** Caramel orange and olive leaf never carry body or label text. They colour icons, rings, dots, bars and pins, always next to a brown word.

## Typography

**Display Font:** Shrikhand (with Georgia, serif)
**Body Font:** Inter 400 / 500 / 600 / 700 (with -apple-system, Segoe UI, Roboto)

**Character:** Shrikhand is the chunky, slanted retro signboard; Inter is the clear menu card beneath it. Inter stays the UI font on both iOS and Android.

### Hierarchy
- **Display** (Shrikhand 400, 34px, 1.12): the wordmark, the 1.1 welcome headline, "Order sent!" (2.9) and "No café can deliver here yet" (3.1, at 28px inside its card). Nowhere else.
- **Headline Large** (Inter 700, 34px, 1.15, -0.02em): tab-root titles ("Orders") and the ETA number ("~2 min").
- **Headline** (Inter 700, 28px, 1.2, -0.015em): screen titles next to the back chevron ("Your cart", "Order #2041").
- **Title** (Inter 600, 22px, 1.25, -0.01em): section headings and bottom-sheet titles (sheets use 700).
- **Body** (Inter 400, 17px, 1.45): running text, sheet copy, chat bubbles, inputs. Buttons use the same 17px at 600.
- **Subhead** (Inter 400, 15px, 1.4): meta lines (distance, time, item count), banner text, privacy notes.
- **Label** (Inter 600, 13px, +0.06em, uppercase): group labels in lists ("IN RANGE · CAN DELIVER TO YOU"). Never above a page heading.
- **Caption / Micro** (Inter 500, 13px / 12px): progress labels, photo tags, tab labels, chat timestamps.

Prices, times, distances and order numbers use tabular figures.

### Named Rules
**The Garnish Rule.** Shrikhand appears only on the wordmark and short headlines of six words or fewer. Never on buttons, prices, labels, numbers or paragraphs.

**The Finnish Room Rule.** Every label, button and headline must survive copy about 30% longer (Finnish is coming): let lines wrap with balance, never truncate actions.

## Layout

Phone-first, iOS frame 390 × 844. Screens are a single vertical column with a 24px side gutter; camera screens and docked bars use 16px. Spacing follows a 4-point grid (4, 8, 12, 16, 20, 24, 32, 40, 48) with half-steps (6, 10, 14) for optical tuning.

Each screen is three bands: the status bar and title at the top, a scrolling content column, and a docked footer with the primary action in thumb reach above the 34px home-indicator inset. Root tabs (Home, Orders, Profile) dock a three-item tab bar instead. Bottom sheets rise over a 42% espresso scrim for anything you must deal with before continuing.

Groups are tight (8–12px inside a card, 12–16px between cards) and sections are separated by 20–32px, with more space above a heading than below it. Lists use hairline-divided rows on white or cream, never cards inside cards. Below 430px the device frame goes full-bleed.

### Named Rules
**The Thumb Zone Rule.** The primary action sits at the bottom of the screen, full width, 56px tall. Tap targets are never smaller than 44 × 44px.

## Elevation & Depth

Gently layered. White surfaces lift off the cream ground with soft, brown-tinted shadows that always carry a downward offset and blur; sheets cast upward. Depth says "this is a thing you can touch", not decoration. Tonal steps (cream → white → sand) do the rest; there are no grey or black shadows and no glow.

### Shadow Vocabulary
- **Card** (`0 1px 2px rgba(74,44,30,.06), 0 6px 16px -6px rgba(74,44,30,.14)`): café cards, order cards, history rows, the courier card, map tags, incoming chat bubbles, icon buttons on photos.
- **Sheet** (`0 -8px 32px rgba(74,44,30,.18)`): bottom sheets and system alerts.
- **Primary** (`0 2px 6px -2px rgba(174,67,30,.45)`): the rust button and send button, a small rust-tinted lift under the one action.
- **Device** (`0 2px 6px rgba(74,44,30,.08), 0 28px 64px -24px rgba(74,44,30,.38)`): mockup frame only.

### Named Rules
**The Warm Shadow Rule.** Every shadow is espresso brown (or rust under the primary button) with a real offset. A zero-offset coloured halo is not depth.

## Shapes

Soft and tactile. Buttons, chips, badges, search and tab pills are full pills (999px). Cards are 20px, inputs and banners 16px, product thumbnails 14px (12px small), bottom sheets 28px on the top corners, the camera viewfinder 24px. Avatars, state icons, radio buttons and map markers are circles; the "your spot" marker on maps is a 7px-rounded square. Outlines are 1.5px (inputs, chips) or 2px (secondary buttons, the live order card); dashed outlines mean "empty" or "out of reach" (out-of-range add buttons, the empty-state card, the unreadable QR frame, the delivery radius).

## Components

### Buttons
Soft, tactile pills you press once.
- **Shape:** full pill (999px), 56px tall, full width in footers; 44px "small" variant beside content.
- **Primary:** roasted rust with white 17px semibold text and the primary shadow. Pressed darkens toward espresso and scales to 0.98.
- **Secondary:** transparent with a 2px espresso inset outline and espresso text; hover/pressed wash the inside with 6% / 12% espresso.
- **Text link:** rust, semibold, underlined 1.5px with a 4px offset; the quiet variant is espresso soft for the least important way out ("Cancel").
- **Disabled:** oat sand ground, espresso-soft text, no shadow.
- **Camera:** on brown screens the primary becomes steamed milk with espresso text and the secondary a cream outline.
- **System:** the neutral espresso button used only inside the mock Apple Pay sheet.

### Chips
- **Style:** white pill, 44px tall, 1.5px espresso-32% outline, 15px medium text.
- **State:** selected chips fill espresso with steamed-milk text. Quick replies in chat use the same chip.

### Cards / Containers
- **Corner Style:** 20px.
- **Background:** porcelain white on the cream ground.
- **Shadow Strategy:** the Card shadow.
- **Border:** none at rest. The live order card adds a 2px espresso inset ring to say "this one is happening now". Out-of-range cafés drop to transparent with a 1.5px outline and stay tappable.
- **Internal Padding:** 12–16px.

### Inputs / Fields
- **Style:** white, 1.5px espresso-32% outline, 16px radius, 56px tall, 17px text, espresso-faint placeholder.
- **Focus:** the outline turns full espresso with a 4px caramel-orange glow at 28%.
- **Error:** rust outline plus a rust caption with an alert icon.
- **Search:** sand-tinted white with no outline and a leading search icon.

### Navigation
- **Back + title:** a 44px back chevron sharing one row with the 28px headline.
- **Tab bar:** three tabs (Home, Orders, Profile) on a near-white bar with a hairline top edge. The active tab gets a caramel-orange pill (60 × 32px) behind a white icon and a semibold espresso label; inactive tabs are espresso soft.
- **Checkout steps:** three numbered circles joined by bars; done steps fill espresso with a check.
- **Underline tabs:** menu categories, with a 3px caramel underline on the selected tab.

### Banners and Privacy Notes
- **Banner:** 16px-radius strip with a leading icon, semibold title and subhead text. Success = white with an olive check circle; warning = white with a 1.5px caramel outline and caramel icon; error = white with a rust outline and rust icon; info = oat sand.
- **Privacy note:** oat-sand box with a shield icon, the first clause in semibold. It always says who sees your photo or location, and for how long.

### Bottom Sheet
Grabber, a 56px icon circle (caramel for warnings, rust for errors), a 22px bold title, 17px espresso-soft copy, then stacked actions: one rust button, one outline button, optionally a quiet text link.

### Live Order Status (signature)
The status card shows the exact time first ("~2 min at 9:51"), then a four-segment progress bar (Received → Preparing → On the way → Delivered) whose current segment gently breathes. Below it, the live map: drawn sand-and-cream streets, a dotted espresso route, the courier as an espresso circle with their initial (pulsing while moving) and you as a caramel pin with a soft halo. A white tag on the map always states "Location shared until delivery".

### Delivered State and Receipt
When the order arrives, the live map gives way to two olive confirmations, "Location sharing stopped" and "Your photo was deleted", so the privacy promise made during tracking is visibly kept. The progress bar turns fully olive and the time becomes the delivery time. Under the map, one track card holds the courier ("Eetu, café staff · Has your photo" + Message) and the receipt row ("3 items · €11.70 ⌄") that opens to the items and the payment. The live map keeps a 220 px floor; the screen scrolls instead of the map shrinking. Past orders open the same delivered layout from "Earlier".

### Order Again, Group Order, Pickup
- **Order again:** a white card at the top of Home with the café, the items and the price, and one small rust "Order again" button with a circular-arrow icon. The same button closes every delivered and past order.
- **Group order:** "Order together" is a chip with a people icon next to the range pill on the menu. The invite sheet holds a QR code on oat sand and one "Share invite link" action. In the group cart, overlapping avatars show who joined (the host in caramel, someone still choosing as a dashed circle), items are grouped under each person, and "Who pays?" is a two-option choice.
- **Pickup:** the order number to show at the counter is the biggest thing on the screen (48px bold, tabular) inside an espresso-ringed white card, followed by the walking map.
- **Map card:** on a full-height walking map, a white card floats at the top with the distance in Title size and the courier's waiting time.

### Camera
Espresso-brown screen, 24px viewfinder with the active camera full size and the other camera live in a white-ringed inset top left. The first shutter press takes the selfie and flips to the back camera (the selfie moves to the inset); the second press takes your spot; then a review screen shows both. A dark translucent hint pill, a cream ring shutter, and warning banners inside the viewfinder.

## Do's and Don'ts

### Do:
- **Do** take every value from `design-system/tokens.css` and every component from `components.css`; screens add layout only.
- **Do** keep exactly one roasted-rust button per screen, docked at the bottom, 56px tall.
- **Do** pair every state colour with an icon and words (olive check + "In range", caramel alert + "Out of delivery range").
- **Do** use espresso soft (#6B5040) for secondary text instead of grey, and keep body text at 4.5:1 or better.
- **Do** show exact times with tabular figures ("9:51 · in ~2 min").
- **Do** write meta lines as facts side by side with the key fact in semibold espresso ("**45 m away**  Open until 18:00"); never start a wrapped line with a separator dot.
- **Do** keep privacy visible wherever a photo or location is shared: who sees it, and until when.
- **Do** use the espresso-brown ground with cream text on camera screens.

### Don't:
- **Don't** use purple gradients, template cards, emoji icons or default fonts.
- **Don't** use moodboard patterns: stripes, halftone dots, checkerboards or badges.
- **Don't** set small text in caramel orange or olive leaf.
- **Don't** use Shrikhand on buttons, prices, labels, numbers or paragraphs.
- **Don't** put a small uppercase label above a page heading, or cards inside cards.
- **Don't** use black or grey anywhere, including camera screens and shadows.
- **Don't** write "our couriers": the courier belongs to the café.
