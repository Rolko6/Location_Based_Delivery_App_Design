# Design Brief – Final (Shoot, customer app)

> Status: **APPROVED – 2026-11-06**
> Builds on `brief.md` and `references/notes.md`; it does not replace them. It records the decisions made in the Q&A on 2026-11-06 and the defaults proposed on top of them.

---

## 1. Scope

**In scope now:** the customer app, iOS, 31 screens from `wireframes/` (sign-up, ordering, café-list edge cases, tracking and messaging, ordering edge cases E1–E10).

**Out of scope until wireframes exist:** Profile tab content, merchant app (M1–M6), runner view. (Group order and "Order again" were designed on 2026-11-07, see 7c.)

**Source priority:** wireframes → brief.md → references/apps → references/inspirations. Layout and content always follow the matching wireframe.

---

## 2. Decisions from the Q&A

| # | Topic | Decision |
|---|---|---|
| 1 | Missing dark / light colors | Borrow **brown `#4A2C1E`** and **cream `#F1E3C6`** from palette 3, only for text and background. Palette 1 stays the brand. |
| 2 | Moodboard | Take only the **feel** (nostalgic, bold, characterful). **No patterns** (no stripes, halftone dots, checkerboard or badges). The UI stays clean. Ignore its palette 3 accents (mustard) and its fonts (Righteous, Bricolage Grotesque). |
| 3 | App name / logo | **"Shoot"** as a text wordmark in Shrikhand, no symbol. Easy to swap later. |
| 4 | Delivery price | Shown as a **separate line**, example amount **€0.50** (café card, cart, checkout, payment sheet). |
| 5 | Content | **Realistic Oulu content:** made-up café names (never real businesses), real products (flat white, oat latte, korvapuusti…), prices in €, phone prefix **+358**, real places (Linnanmaa, Hupisaaret, Kauppatori). UI language: English. |
| 6 | Delivery radius | **Every café has its own radius** (set by the owner). Example cafés use **100 m**. Screen 1.5 uses a general phrase ("within a short walk") instead of a number. |
| 7 | Platform | Mockups show **iOS**: iPhone frame 390 × 844, Apple Pay, Face ID, iOS-style system dialogs and sheets. Android comes later as a variant. |
| 8 | UI font on native | **Inter** stays the UI font on both iOS and Android (not SF Pro / Roboto). |
| 9 | Appearance | **Light mode only** for now. No dark mode. |
| 10 | Design tokens | All design values live in `design-system/tokens.css`. Screens use only its CSS variables, never hardcoded values. |
| 11 | Shared components | Component styles live in `design-system/components.css`, icons in `design-system/icons.js`. Screens reuse them and add layout only. |

---

## 3. Colors

### Palette
| Token | Hex | Source | Role |
|---|---|---|---|
| `orange` | `#D06224` | palette 1 | Brand accent: wordmark, highlights, active tab, selected chip, progress/ETA accents, map pin |
| `rust` | `#AE431E` | palette 1 | **Primary action buttons** (with cream/white text), links, error text |
| `olive` | `#8A8635` | palette 1 | Positive / "in range" / delivered: icons, check circles, progress fill, status dots |
| `sand` | `#E9C891` | palette 1 | Secondary surfaces: info boxes, chips, inactive progress segments, illustration fills |
| `cream` | `#F1E3C6` | palette 3 | **App background** |
| `brown` | `#4A2C1E` | palette 3 | **All text and icons**, secondary (outline) buttons, camera-screen background |
| `white` | `#FFFFFF` | – | Cards and sheets on the cream background |

Primary buttons use **rust**, not orange. Orange with white text only reaches 3.85:1, which passes AA for large text only. Rust passes AA at any size, and orange stays the brand accent.

Camera screens (2.4, 2.4b, 2.5, 2.6, E3, E4, E5) keep the wireframes' dark layout but use **brown `#4A2C1E`** instead of black, with cream text.

Secondary text uses brown at reduced strength (about 75% opacity on cream), and it must stay ≥ 4.5:1. No grey.

### Contrast check (WCAG AA)
| Text / foreground | Background | Ratio | Use |
|---|---|---|---|
| brown | cream | 9.91 | ✅ body text |
| brown | white | 12.57 | ✅ text on cards |
| brown | sand | 7.86 | ✅ text in info boxes / chips |
| cream | brown | 9.91 | ✅ text on camera screens |
| white | rust | 5.80 | ✅ primary button text |
| cream | rust | 4.57 | ✅ primary button text |
| rust | cream | 4.57 | ✅ links, error text |
| white | orange | 3.85 | ⚠️ large/bold text ≥ 18.66 px only (badges, big numbers) |
| brown | orange | 3.27 | ⚠️ large text only |
| olive | cream | 2.99 | ❌ never for text. Icons only, always paired with a brown label |
| olive | white | 3.79 | ✅ non-text (icons, check circles) on white cards |

**Status colors:** success / in range = olive icon + brown label · error = rust · warning = orange icon + brown text · neutral info = sand box + brown text.

---

## 4. Typography

- **Shrikhand** (Google Fonts): wordmark and **short large headlines only**. Never paragraphs, buttons, prices, labels or numbers.
  - Used on: the wordmark (1.1), the 1.1 hero headline, 2.9 "Order sent!", 3.1 "No café can deliver here yet". All other headings use Inter.
- **Inter** 400 / 500 / 600 / 700 (Google Fonts): the entire UI.
- Base scale (px): 34 / 28 / 22 / 17 / 15 / 13. Body 17 px. Buttons 17 px semibold. Small-caps section labels (e.g. "IN RANGE · CAN DELIVER TO YOU") 13 px semibold with letter-spacing, as in the wireframes.
- Both fonts load from Google Fonts in HTML mockups. `assets/fonts/` (React Native) does not exist yet.

---

## 5. Visual style

- **Feel:** Starbucks-calm (lots of space, one clear action per screen, short copy) + Bolt-Food arrangement (spacing rhythm, primary button at the bottom in thumb reach) + insp-4/5 look (cream + brown, rounded pill buttons, rounded cards, rounded tab-bar icons, map + timeline when tracking).
- **Shapes:** pill-shaped buttons and chips. Rounded cards (20 px radius). Bottom sheets with a grab handle (as in E1, E5, E7, E8, E10).
- **Icons:** simple rounded line icons in brown. No emoji.
- **Illustrations:** simple one-stroke line-art characters in brown (style of insp-1/2/3, no neon colors). Mockups use **simple placeholders**; final art comes from a licensed pack or our own drawings.
  - Placed where the wireframes have an illustration or circle slot: 1.1 (illustration box), 1.5 (circle), 2.9 (check circle → character + check), 3.1 (circle). Error sheets keep the wireframes' icon-in-circle.
- **Avoid:** purple gradients, template-looking cards, emoji icons, default fonts, moodboard patterns, references' brand colors.
- **Touch:** tap targets ≥ 44 pt, primary actions at the bottom, everything usable with one hand.

---

## 6. Content rules

- Say "**courier**", never "our couriers". The courier belongs to the café.
- Privacy copy stays visible where the wireframes have it (2.3, 2.4, 2.5, E2): the photo is shared only with the café, only for this order.
- Order status labels: **Received → Preparing → On the way → Delivered**. (Wireframe said "Prepared"; changed on 2026-11-07 after the critique so the current step reads as in progress, not done.)
- Wireframe prototype links such as "[prototype: photo is blurry]" are **not** shown in the mockups. The edge cases are designed as their own screens.
- E8 refund decided on 2026-11-07 (see 7c); the placeholder is gone.

---

## 7. Screen list and build order

One screen at a time, saved as HTML in `screens/`. Wait for feedback after each screen.

**UC-01 Sign-up:** 1.1 Welcome · 1.2 Phone number · 1.3 SMS code · 1.4 Location permission (iOS system alert over a pre-permission screen) · 1.5 Location denied · 1.6 Café list (home)

**UC-02 Ordering:** 2.1 Café menu · 2.2 Cart · 2.3 Confirm your spot · 2.4 Photo (first press: selfie; the other camera is always live in the top-left inset) · 2.4b Photo – second press: your spot · 2.5 Photo review (always shown; also opened from the 2.7 thumbnail) · 2.6 Scan spot QR · 2.7 Checkout (Apple Pay selected) · 2.8 Apple Pay sheet · 2.9 Order sent · 2.10 Orders

**UC-03 Café list – edge cases:** 3.1 No café in range · 3.2 Menu – browse only

**UC-04 Tracking & messaging:** 4.1 Orders tab · 4.2 Order status · 4.3 Message the courier

**UC-02 Ordering – edge cases (states/sheets, reuse main-flow components):** E1 Moved out of range · E2 Camera access denied · E3 Photo blurry · E4 QR can't be read · E5 QR not valid here · E6 Item sold out · E7 Payment failed · E8 Left the area while preparing · E9 Courier can't find you · E10 Update my spot

Notes:
- **2.10 and 4.1 are identical wireframes.** Design once (as 2.10) and reuse it for 4.1.
- Bottom tab bar: **Home · Orders · Profile**. The Profile tab is shown in the bar but not designed.
- Wireframes 2.6 and E4 have a secondary button whose text is unreadable ("No code here? Take a photo instead" / "Take a photo instead"). It will be designed readable.

---

## 7b. Flow changes after the critique (2026-11-07)

- **2.3 Confirm your spot is shown on the first order only.** Repeat orders go from the cart straight to the camera (2.4); the camera note carries the privacy line ("Only [café] sees them, for this order"). The prototype remembers a completed order (2.9) and then skips 2.3. Reusing the last photo is not possible: it is deleted at delivery.
- **Both photos are taken by hand** (changed again on 2026-11-07 at the user's request): the first press takes the selfie and flips the view to the back camera (selfie moves to the inset), the second press takes your spot. No countdown.
- **2.5 Photo review is always shown** after the second photo, so the customer can check both before checkout. The 2.7 thumbnail also opens 2.5. A blurry photo opens E3.
- **The Apple Pay sheet names the café as the merchant** ("Pay Saaripaahtimo"), not Shoot.
- **2.9 Order sent is a short success moment** (~3 s) that shows the handoff instead of a receipt (the café has your photo, step 1 of 4, ETA) and then opens tracking (4.2) by itself; "Track order" goes there at once.
- **Meta lines have no separator dots.** Facts sit side by side and wrap whole; the key fact (distance, ready time) is semibold ink, the rest secondary. One distance per café across the flow (Saaripaahtimo: 45 m).
- **4.2b Order delivered** (decided 2026-11-07): the end state of tracking. Full olive progress, "Delivered to your spot · 9:51", and in place of the map two olive confirmations: "Location sharing stopped" and "Your photo was deleted" (the photo is deleted at delivery). Chat closes. Answers C8 (Laura).
- **Former dead links now open sheets:** "Map" on 2.3 → 2.3b Your spot on the map (with the location privacy line); "?" in the camera → 2.4c Photo tips.

## 7c. Decisions on 2026-11-07 (group order, reorder, refund)

- **Group order (C2, C3):** the host starts it from the menu ("Order together"), shares a link or QR code, friends add their own items, and the host chooses who pays: "I'll pay for everyone" or "Everyone pays for their own". One delivery to the host's spot; only the host takes the photo.
- **Order again (C5):** a card at the top of Home (1.6) with the last order and one tap back to a filled cart, plus an "Order again" button on delivered and past orders.
- **Refund (E8):** full refund while the order is only Received; once the café is Preparing there is no refund, only "go back to my spot" or "pick it up at the counter". Matches E9 ("already made").
- **Pick up at the counter (4.5):** shows the order number to show at the counter, the walk to the café, and that location sharing stopped.

## 8. Still open (not blocking the customer-app mockups)

- Runner phase: who assigns orders when a café has more than one runner?
