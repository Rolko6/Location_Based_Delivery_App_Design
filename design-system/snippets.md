# Shared markup snippets

Copy these into screens. Styling lives in `components.css`; values in `tokens.css`.
Drawing coordinates inside SVGs (viewBox, path data, stroke widths in user units) are geometry, not design tokens.

## Map preview (`.map`)

```html
<div class="map" role="img" aria-label="Map preview: you are inside the café's delivery radius">
  <svg viewBox="0 0 268 120" preserveAspectRatio="xMidYMid slice" aria-hidden="true">
    <path class="park" d="M0 78C30 70 60 86 84 120H0Z"/>
    <path class="park" d="M196 0c8 22 40 30 72 26V0Z"/>
    <path class="road" stroke-width="10" d="M-10 44c70 8 160-14 290 4"/>
    <path class="road" stroke-width="6" d="M120-10c-2 50 12 90 6 140"/>
    <path class="road" stroke-width="4" d="M190 130c6-40 30-60 90-46"/>
    <path class="road" stroke-width="4" d="M-10 100c50-4 90 4 134-4"/>
    <circle class="radius" cx="134" cy="62" r="40"/>
    <circle class="cafe-dot" cx="158" cy="40" r="5"/>
    <circle class="pin" cx="134" cy="62" r="7"/>
  </svg>
</div>
```

## Location illustration placeholder (`.illo.illo-round`)

`assets/illustrations/location.svg` does not exist yet. Until it does, 1.4 and 1.5 use this line-art placeholder.

```html
<figure class="illo illo-round" role="img" aria-label="Map pin inside its delivery radius">
  <svg class="art" viewBox="0 0 160 160" aria-hidden="true">
    <ellipse class="dashed drift" cx="80" cy="128" rx="58" ry="12"/>
    <path class="fill-cream" d="M80 124c-5-7-36-38-36-64a36 36 0 0 1 72 0c0 26-31 57-36 64z"/>
    <circle class="fill-orange" cx="80" cy="60" r="13"/>
  </svg>
</figure>
```

## Number keyboard (`.keyboard`)

```html
<div class="keyboard" aria-hidden="true">
  <!-- optional QuickType bar: <button class="suggest"><small>From Messages</small><strong>481 236</strong></button> -->
  <div class="keys">
    <button class="key" data-key="1">1<small>&nbsp;</small></button>
    <button class="key" data-key="2">2<small>ABC</small></button>
    <button class="key" data-key="3">3<small>DEF</small></button>
    <button class="key" data-key="4">4<small>GHI</small></button>
    <button class="key" data-key="5">5<small>JKL</small></button>
    <button class="key" data-key="6">6<small>MNO</small></button>
    <button class="key" data-key="7">7<small>PQRS</small></button>
    <button class="key" data-key="8">8<small>TUV</small></button>
    <button class="key" data-key="9">9<small>WXYZ</small></button>
    <span class="key blank"></span>
    <button class="key" data-key="0">0</button>
    <button class="key fn" data-key="del" aria-label="Delete"><svg class="i"><use href="#i-delete"/></svg></button>
  </div>
</div>
```
