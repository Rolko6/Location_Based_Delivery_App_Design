# Product

<!-- impeccable:product-schema 1 -->

## Platform

adaptive

## Stack

- Product: React Native, one codebase for iOS and Android. The design follows each OS's native conventions where it matters (system dialogs, payment sheets, permissions, navigation gestures).
- Current deliverable: static HTML/CSS mockups, one file per screen, saved in `screens/`. iOS first (iPhone frame 390 × 844, Apple Pay, Face ID); Android variants later.

## Users

Primary user: someone who is **staying where they are** near a café and wants coffee or food brought to them without leaving that spot.

- **Aino** (21, CS student, Linnanmaa campus): in a team meeting on a bench or in a common area; the café queue would cost her spot and focus. Wants to order for the whole team, low fees.
- **Mikko** (29, freelance developer, Hupisaaret park): minutes between calls; wants a few taps, Apple Pay, an exact delivery time, no phone calls, one-tap repeat of his usual order.
- **Laura** (34, parent on leave, playground): can't leave her kids; has the phone in one hand for a few seconds at a time. Needs a very simple flow, confidence the courier will find her, and visible privacy.

Other audiences (merchant app and runner view are not designed yet):
- **Sanna** (38, café owner near Kauppatori, 2 baristas per shift): wants orders from people nearby without platform commissions; sets delivery radius, pauses orders in a rush, marks items sold out.
- **Barista**: prepares and sometimes carries orders; needs to see *who* (photo) and *where* (live location) at a glance.
- **Runner** (phase 2): carries orders for one café all day.

## Product Purpose

Hyper-local ordering: the café itself brings coffee and food to wherever the customer is right now, within a short walk of the café (each café sets its own radius; examples use 100 m). Modules: customer app (find nearby cafés, order, pay, get it delivered to your spot), merchant app / dashboard, and runner view (phase 2).

Success: a customer gets from opening the app to a paid order in as few steps as possible, and the café finds them on the first try.

## Positioning

- **Short distances only** (roughly 50–200 m). Big delivery platforms make no sense for orders under 100 m.
- **The café delivers, not a courier platform**: no high commissions, no strangers chasing orders.
- **Photo + live location per order**: the customer takes a quick front + back camera photo so the barista or runner recognises them and their spot in a crowded place. At a table or marked spot, a QR code replaces the photo.
- **No kiosks or extra seats** for the café: the whole area around it becomes ordering "seats" through an app customers already know how to use.

## Operating Context

- Location: Oulu, Finland: Linnanmaa campus, Hupisaaret park, Kauppatori market square. Outdoor use in sunlight, crowds, one hand busy.
- Customer flow: sign-up (phone + SMS code + location permission only) → café list (in range / out of range) → menu → cart → confirm your spot (photo, or scan the spot's QR code) → checkout → Apple Pay / Google Pay → order sent → live tracking (Received → Preparing → On the way → Delivered) → in-app messages with the courier.
- Communication happens in the app (status updates, short messages, quick replies). No phone calls.
- Out of range: the menu stays browsable but ordering is disabled. If the customer moves out of range or leaves the area while the order is prepared, the app says so and lets them update their spot.

## Capabilities and Constraints

- Sign-up is phone number + SMS code + location permission, nothing else. The photo is taken per order, never during sign-up.
- The photo is proof of location; it is shared only with that café, only for that order, and **deleted when the order is delivered**. Location sharing stops at delivery too; the Delivered screen says both.
- Payment: Apple Pay / Google Pay, saved cards.
- Delivery fee is shown as a separate line (example amount €0.50).
- **Terminology:** say "courier" in the customer UI, never "our couriers". The courier belongs to the café; any employment agreement is between the café and the runner, never the platform.
- **Not designed until wireframes exist:** Profile tab, merchant app, runner view.
- **Group order:** the host shares a link / QR code, friends add their own items, the host chooses who pays (one for all, or each their own). One delivery, one photo (the host's).
- **Refunds:** full refund while an order is only Received; none once the café is preparing (pick-up at the counter instead).
- **Undecided:** runner order assignment when a café has several runners.
- Language: English now, **Finnish to be added later**. Copy and layouts must leave room for longer Finnish words.

## Brand Commitments

- Working name: **Shoot** (wordmark only, no symbol yet).
- Customer-app structure, content and flow come from the user's wireframes in `wireframes/`; they override every reference.
- Visual decisions (palette, fonts, style) are recorded in `brief.md` and `design-brief-final.md` (approved 2026-11-06).

## Evidence on Hand

- This is a **student / concept project** (University of Oulu software project). There are no real café partners, users, orders, ratings, testimonials or metrics.
- Never fabricate partner cafés, user counts, reviews, ratings or press. Café names in mockups are invented and must not be real Oulu businesses.
- Sources: `brief.md` (personas, user stories), `wireframes/` (31 customer-app screens), `references/` (Mobbin onboarding flows: Starbucks, Bolt Food, Panera; Pinterest inspiration), `moodboard/`, `color_palettes/`.

## Product Principles

1. **Stay where you are.** Every decision protects the customer's spot and attention: few steps, primary action in thumb reach, usable one-handed in seconds.
2. **The handoff is the product.** The photo/QR + location step must be fast for the customer and unmistakable for the barista or runner.
3. **Exact, not vague.** Show a concrete ETA and a live four-step status; no phone calls.
4. **Privacy you can see.** Always make clear what is shared, with whom, and for how long.
5. **The café stays in charge.** The café delivers with its own people; the platform never stands between them.

## Accessibility & Inclusion

- WCAG AA text contrast (required by the brief).
- One-handed use: large tap targets (≥ 44 pt) in the thumb zone; primary actions at the bottom.
- Readable outdoors in sunlight and usable in a few-second glance (Laura).
