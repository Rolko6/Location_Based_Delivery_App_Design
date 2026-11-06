# Design Brief – Shoot

> Source of truth for all design work in this folder. Read this first, then the folders listed under "Sources".
> Personas and user stories come from our Figma board. Items marked *(new)* are not in Figma yet.

---

## 1. What the app is

A cross-platform (React Native, iOS + Android) app for **hyper-local ordering from cafés**: coffee and food brought by the café itself to wherever the customer is right now (a campus bench, a park, a playground, a terrace or a table inside the café).

**Modules**
1. **Customer app**: find nearby cafés, order, pay (Apple Pay / Google Pay) and get it delivered to your spot.
2. **Merchant app / dashboard**: café owner and baristas manage the menu, availability, delivery radius and incoming orders.
3. **Runner view (phase 2)**: the person carrying orders from the café to customers nearby.

**What makes it different**
- **Short distances.** We deliver within roughly 50–200 m of the café, not across the city. Big delivery platforms don't make sense for orders under 100 m.
- **The café delivers, not a courier platform.** No high commissions and no strangers chasing orders.
- **Photo + live location.** The customer takes a quick photo of themselves or their surroundings, so the barista or runner finds them on the first try in a crowded place.
- **No kiosks or extra seats needed.** The café gets self-ordering and "seats" in the whole area around it through an app customers already know how to use.
- **Ordering for a group.** Friends or a team can add their drinks into one order.

**Location context:** Oulu, Finland (Linnanmaa campus, Hupisaaret park, Kauppatori market square).

---

## 2. Personas

### Persona 1 – Aino, "Student at campus"
- 21, computer science student, University of Oulu, Linnanmaa campus
- Spends the day between lectures and team projects. The team often meets on a bench or in a common area. The nearest café is a 5-minute walk away and always has a queue. If she leaves, she loses her spot and her focus.
- **Goals:** get coffee without interrupting a meeting, order for the whole team at once, avoid high fees
- **Frustrations:** queues during breaks, expensive delivery apps that can't find her on campus

### Persona 2 – Mikko, "Remote worker in the park"
- 29, freelance developer, Hupisaaret Islands park, Oulu
- Works from the park with his laptop when the weather is good. He has only a few minutes between calls and doesn't want to pack up just to get coffee. He expects to order in a few taps with Apple Pay.
- **Goals:** repeat his usual order with one tap, know the exact delivery time
- **Frustrations:** long onboarding, unclear delivery times, phone calls from the courier

### Persona 3 – Laura, "Parent at the playground"
- 34, on parental leave, playground in a park, Oulu
- Takes her kids to the playground every day. The café is 70 m away, but she can't leave the children alone. She only has her phone in hand for a few seconds at a time, so the app has to be very simple.
- **Goals:** get coffee without leaving the kids, use the app with one hand, be sure the courier will find her
- **Frustrations:** complicated menus, a crowded park, privacy concerns

### Persona 4 – Sanna, "Café owner"
- 38, owns a small café with a terrace near Kauppatori (Market Square), 2 baristas per shift
- The park is full of people, but only some of them come into her café. Large delivery platforms take high commissions and make no sense for deliveries under 100 m. She wants to reach people nearby and have the coffee brought to them by herself or a barista.
- **Goals:** more orders without couriers, set a delivery radius, quickly update the menu and availability
- **Frustrations:** high commissions, order rushes, customers she can't find

### Supporting role – Barista
- Works in the café during a shift, prepares orders and sometimes carries them out.
- Needs to see **who** the order is for (photo) and **where** they are (live location) at a glance.

### Supporting role – Runner *(new)*
- Carries orders from one café to customers nearby.
- Prefers to **work at the same café for the whole day** rather than chase orders around the city for Wolt-style platforms.
- **Legal note:** any employment or part-time agreement is between the **café and the runner**. The platform never has agreements with runners. In the customer UI we say "courier" (as in the wireframes), but never "our couriers": the courier belongs to the café.

---

## 3. User stories

### Customer
| ID | Persona | Story |
|---|---|---|
| C1 | Aino | As a student, I want to order coffee to my bench on campus, so that I don't have to leave my team meeting. |
| C2 | Aino | As a student, I want to create a group order, so that my whole team can add their drinks at once. |
| C3 | Customer *(new)* | As a customer, I want to sit down with my friends and make one order for everyone. |
| C4 | Mikko | As a remote worker, I want to see the exact delivery time, so that I know if it arrives before my next call. |
| C5 | Mikko | As a remote worker, I want to repeat my last order with one tap, so that I can get coffee between calls. |
| C6 | Laura | As a parent, I want to order and take the photo with one hand, so that I can keep watching my kids. |
| C7 | Laura | As a parent, I want the barista to see my photo and surroundings, so that they find me in a crowded park. |
| C8 | Laura | As a parent, I want my location sharing to stop after delivery, so that I feel safe using the app. |

### Café owner / barista
| ID | Persona | Story |
|---|---|---|
| M1 | Sanna | As a café owner, I want to set my delivery radius, so that I only get orders we can walk to. |
| M2 | Sanna | As a café owner, I want to pause orders during a rush, so that we don't fall behind. |
| M3 | Sanna | As a café owner, I want to mark items as sold out, so that customers can't order what we don't have. |
| M4 | Barista | As a barista, I want to see the customer's photo and live location, so that I find them on the first try. |
| M5 | Café owner *(new)* | As a café owner, I don't want to invest in self-order machines or kiosks. I want a scalable app, so customers can find a seat or table and order with a UX they're already used to. |
| M6 | Café owner *(new)* | As a café owner, I don't want to invest in more customer seats. I want to deliver great coffee to people around the café instead. |

### Runner
| ID | Persona | Story |
|---|---|---|
| R1 | Runner *(new)* | As a runner, I prefer working at the same café for the whole day, so that I don't have to chase platform orders and drive around the city. |

---

## 4. What this means for the design

- **One-handed and fast (Laura, Mikko).** Big tap targets in the thumb zone, primary actions at the bottom, as few steps as possible from opening the app to paying.
- **Reorder is a first-class action (Mikko).** "Order again" is visible on the home screen, not hidden in history.
- **Exact time, not a vague estimate (Mikko).** Show a clear ETA and a live status: accepted → preparing → on the way → delivered.
- **The handoff is the critical moment (Laura, barista, Sanna).** The photo + location step must be quick for the customer and very clear for the barista or runner.
- **Privacy is visible (Laura).** Make it obvious when location is shared and that it stops after delivery.
- **No phone calls (Mikko).** Communication goes through the app (status updates, short in-app messages).
- **Group order (Aino, C3).** One person starts the order, others join through a link or QR code and add their items, then one person pays (or everyone pays separately, still open).
- **Merchant UI is for busy hands (Sanna, barista).** Large toggles for "pause orders" and "sold out", and new orders that are easy to read at a glance during a rush.
- **Two ways to set your spot.** Outside: confirm your spot + a photo (front or back camera) so the courier finds you. At a table or marked spot: scan the spot's QR code.
- **Sign-up is short (Mikko).** Phone number + SMS code + location permission, nothing else. The photo is taken per order, not during sign-up.
- **Range matters.** Out of range, the menu is still browsable but ordering is disabled. If you move out of range or leave the area while the order is being prepared, the app tells you and lets you update your spot.

---

## 5. Colors

- Palettes are in `colorpallets/` (versions 1–4).
- **First choice: `color_palette_1.png`.** Start with this one.
- Use the others only for comparison when I ask.
- Read the hex codes from the image and suggest roles: primary, accent, background, surface, text and status colors.
- Check text contrast (WCAG AA).

## 6. Typography

- **Logo and large headlines:** **Shrikhand** (Google Fonts). Use it sparingly, only for short texts. Never use it for paragraphs, buttons or prices.
- **The whole UI:** **Inter** (Google Fonts), weights 400 / 500 / 600 / 700.
- In HTML mockups, load both from Google Fonts.
- Font files for React Native are in `assets/fonts/`.

---

## 7. Sources

- `moodboard/`: visual direction
- `wireframes/`: PNG exports of my customer-app wireframes (see section 8 for the file list). **Follow their structure.**
- `references/apps/`: real apps (Mobbin) – use for UX patterns
- `references/inspiration/`: Pinterest concepts – use ONLY for visual mood, not layouts
- `references/notes.md`: what I like / don't like and which screens each reference is for
- `colorpallets/`: color palettes (1 = first choice)

---

## 8. Screens – Customer app (from my wireframes)

Wireframes are PNG exports in `wireframes/`, named by use case. **Each mockup must follow the structure of its wireframe.** When you design a screen, open the matching file first.
Build in the order below: main flow first, then edge cases.

### UC-01 Sign-up
| ID | File | Screen |
|---|---|---|
| 1.0 | – (no wireframe – designed in `screens/`) | Splash (animated) |
| 1.1 | `1.1-welcome.png` | Welcome |
| 1.2 | `1.2-phone-number.png` | Phone number |
| 1.3 | `1.3-sms-code.png` | SMS code |
| 1.4 | `1.4-location-permission.png` | Location permission |
| 1.5 | `1.5-location-denied.png` | Location denied |
| 1.6 | `1.6-cafe-list-home.png` | Café list (home) |

### UC-02 Ordering
| ID | File | Screen |
|---|---|---|
| 2.1 | `2.1-cafe-menu.png` | Café menu |
| 2.2 | `2.2-cart.png` | Cart |
| 2.3 | `2.3-confirm-your-spot.png` | Confirm your spot |
| 2.4 | `2.4-photo-front-back.png` | Photo (front / back camera) |
| 2.5 | `2.5-photo-review.png` | Photo review |
| 2.6 | `2.6-scan-spot-qr.png` | Scan spot QR |
| 2.7 | `2.7-checkout-payment-method.png` | Checkout – payment method |
| 2.8 | `2.8-apple-google-pay-sheet.png` | Apple Pay / Google Pay sheet |
| 2.9 | `2.9-order-sent.png` | Order sent |
| 2.10 | `2.10-orders.png` | Orders |

### UC-03 Café list – edge cases
| ID | File | Screen |
|---|---|---|
| 3.1 | `3.1-no-cafe-in-range.png` | No café in range |
| 3.2 | `3.2-menu-browse-only.png` | Menu – browse only (out of range) |

### UC-04 Tracking & messaging
| ID | File | Screen |
|---|---|---|
| 4.1 | `4.1-orders-tab.png` | Orders tab |
| 4.2 | `4.2-order-status.png` | Order status |
| 4.3 | `4.3-message-courier.png` | Message the courier |

### UC-02 Ordering – edge cases
| ID | File | Screen |
|---|---|---|
| E1 | `E1-moved-out-of-range.png` | Moved out of range |
| E2 | `E2-camera-access-denied.png` | Camera access denied |
| E3 | `E3-photo-blurry.png` | Photo blurry |
| E4 | `E4-qr-cant-be-read.png` | QR can't be read |
| E5 | `E5-qr-not-valid-here.png` | QR not valid here |
| E6 | `E6-item-sold-out.png` | Item sold out |
| E7 | `E7-payment-failed.png` | Payment failed |
| E8 | `E8-left-area-while-preparing.png` | Left the area while preparing |
| E9 | `E9-courier-cant-find-you.png` | Courier can't find you |
| E10 | `E10-update-my-spot.png` | Update my spot |

Edge cases reuse the components of the main flow (same cards, buttons, sheets). Design them as states or sheets, not as new layouts.

### Not wireframed yet (don't design until I add wireframes)
- Group order (C2, C3)
- "Order again" / one-tap reorder (C5)
- Merchant app: incoming orders, delivery radius, pause orders, sold out (M1–M4)
- Runner view (phase 2)

---

## 9. Open questions (ask me about these)

- App name and logo (working title Shoot)
- Delivery price: included in the product price or shown separately?
- Group order payment: one person pays, or split?
- Runner phase: who assigns orders when a café has more than one runner?

---

## 10. Rules for the agent

- Mobile-first, iOS and Android.
- My materials are the source of truth. Don't invent features or content. **Ask instead.**
- Ask one question at a time and wait for my answer.
- No generic AI design (purple gradients, template cards, emoji as icons, default fonts).
- Build one screen at a time and wait for my feedback after each.
- Save mockups as HTML in `screens/`.