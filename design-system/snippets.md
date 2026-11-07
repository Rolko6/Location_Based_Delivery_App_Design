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

## "You" inset (`.pip`)

The woman from the unDraw "Selfie" illustration, cropped to head and shoulders. Stands in for the front-camera photo.

```html
<div class="pip"><svg class="illo-color" viewBox="329 50 244 333" preserveAspectRatio="xMidYMin slice" aria-hidden="true" focusable="false"><g transform="translate(-655 -180)"><path d="M864.338,196.984V644a35.264,35.264,0,0,1-35.272,35.268H655.35A35.266,35.266,0,0,1,620.083,644V196.984a35.266,35.266,0,0,1,35.269-35.268h21.081A16.755,16.755,0,0,0,691.945,184.8h99.048A16.762,16.762,0,0,0,806.5,161.716h22.567a35.266,35.266,0,0,1,35.267,35.269Z" transform="translate(363.972 30.573)" class="screen"/>
<path d="M312.558,263.319l-14.052,31.01-25.691,56.7V250.739Z" transform="translate(711.238 231.688)" class="skin"/>
<path d="M812.454,327.594c0,42.461-39.262,36.039-87.7,36.039s-87.7,6.422-87.7-36.039,19.179-117.728,87.7-117.728C795.636,209.866,812.454,285.132,812.454,327.594Z" transform="translate(367.472 40.499)" class="ink"/>
<path d="M304.558,542.65s20.849,29.268,13.4,37.192,55.862,8.122,55.862,8.122-9.51-42.576-6.711-52.374Z" transform="translate(764.952 -148.376)" class="skin"/>
<path d="M828.135,435.73l3.2,19.974V593.408a35,35,0,0,1-4.571,17.369l-32.107-56.291L783.085,436.6,780.2,407.156l43.505.917Z" transform="translate(396.979 81.168)" class="skin"/>
<path d="M864.338,441.834c-1.544-5.018-4.161-13.5-7.164-22.953-5.283-16.657-11.748-36.377-15.583-45.773-7.321-17.935-44.627-10.747-44.627-10.747l-127.815-4.788s-4.764-.627-26.2-3.474c-8.986-1.194-16.814,11.4-22.868,26.439v47.341l29.78,2.268a107.475,107.475,0,0,0-4.089,25.655c-.338,11.88,1.761,25.16,10.819,33.4C676.12,507,682.4,587.138,682.4,587.138l-13.738,52.491h160.4a35.264,35.264,0,0,0,35.267-35.272V584.919c-10.12-16.379-18.43-24.617-18.43-24.617L817.214,447.443l43.928-.76,3.2-.06Z" transform="translate(363.971 70.215)" class="ink"/>
<circle cx="59.01" cy="59.01" r="59.01" transform="translate(1012.641 340.754) rotate(-45)" class="skin"/>
<path d="M653,294.246h23.34l10.3-28.831,2.059,28.831h11.156l6.006-16.818,1.2,16.818h82.89a62.468,62.468,0,0,0-62.468-62.468H715.468A62.468,62.468,0,0,0,653,294.245Z" transform="translate(370.757 45.016)" class="ink"/></g></svg></div>
```

## Mock QR sticker (`.qr-code`)

Not a real code. Shown inside `.qr-frame` on 2.6.

```html
<svg class="qr-code" viewBox="-2 -2 25 25" aria-hidden="true" focusable="false"><rect class="light" x="-2" y="-2" width="25" height="25" rx="2"/><rect x="0" y="0" width="7" height="7"/><rect class="light" x="1" y="1" width="5" height="5"/><rect x="2" y="2" width="3" height="3"/><rect x="14" y="0" width="7" height="7"/><rect class="light" x="15" y="1" width="5" height="5"/><rect x="16" y="2" width="3" height="3"/><rect x="0" y="14" width="7" height="7"/><rect class="light" x="1" y="15" width="5" height="5"/><rect x="2" y="16" width="3" height="3"/><rect x="8" y="0" width="1" height="1"/><rect x="9" y="0" width="1" height="1"/><rect x="11" y="0" width="1" height="1"/><rect x="8" y="1" width="1" height="1"/><rect x="9" y="1" width="1" height="1"/><rect x="11" y="1" width="1" height="1"/><rect x="12" y="1" width="1" height="1"/><rect x="8" y="2" width="1" height="1"/><rect x="9" y="2" width="1" height="1"/><rect x="10" y="2" width="1" height="1"/><rect x="12" y="2" width="1" height="1"/><rect x="8" y="3" width="1" height="1"/><rect x="12" y="3" width="1" height="1"/><rect x="9" y="4" width="1" height="1"/><rect x="11" y="4" width="1" height="1"/><rect x="12" y="4" width="1" height="1"/><rect x="8" y="5" width="1" height="1"/><rect x="9" y="5" width="1" height="1"/><rect x="11" y="5" width="1" height="1"/><rect x="9" y="6" width="1" height="1"/><rect x="11" y="6" width="1" height="1"/><rect x="12" y="6" width="1" height="1"/><rect x="8" y="7" width="1" height="1"/><rect x="10" y="7" width="1" height="1"/><rect x="11" y="7" width="1" height="1"/><rect x="0" y="8" width="1" height="1"/><rect x="1" y="8" width="1" height="1"/><rect x="4" y="8" width="1" height="1"/><rect x="9" y="8" width="1" height="1"/><rect x="11" y="8" width="1" height="1"/><rect x="12" y="8" width="1" height="1"/><rect x="14" y="8" width="1" height="1"/><rect x="16" y="8" width="1" height="1"/><rect x="0" y="9" width="1" height="1"/><rect x="4" y="9" width="1" height="1"/><rect x="7" y="9" width="1" height="1"/><rect x="9" y="9" width="1" height="1"/><rect x="14" y="9" width="1" height="1"/><rect x="15" y="9" width="1" height="1"/><rect x="17" y="9" width="1" height="1"/><rect x="18" y="9" width="1" height="1"/><rect x="19" y="9" width="1" height="1"/><rect x="20" y="9" width="1" height="1"/><rect x="0" y="10" width="1" height="1"/><rect x="2" y="10" width="1" height="1"/><rect x="3" y="10" width="1" height="1"/><rect x="4" y="10" width="1" height="1"/><rect x="6" y="10" width="1" height="1"/><rect x="7" y="10" width="1" height="1"/><rect x="12" y="10" width="1" height="1"/><rect x="13" y="10" width="1" height="1"/><rect x="14" y="10" width="1" height="1"/><rect x="17" y="10" width="1" height="1"/><rect x="18" y="10" width="1" height="1"/><rect x="19" y="10" width="1" height="1"/><rect x="20" y="10" width="1" height="1"/><rect x="2" y="11" width="1" height="1"/><rect x="3" y="11" width="1" height="1"/><rect x="4" y="11" width="1" height="1"/><rect x="5" y="11" width="1" height="1"/><rect x="12" y="11" width="1" height="1"/><rect x="17" y="11" width="1" height="1"/><rect x="18" y="11" width="1" height="1"/><rect x="19" y="11" width="1" height="1"/><rect x="0" y="12" width="1" height="1"/><rect x="1" y="12" width="1" height="1"/><rect x="2" y="12" width="1" height="1"/><rect x="3" y="12" width="1" height="1"/><rect x="4" y="12" width="1" height="1"/><rect x="5" y="12" width="1" height="1"/><rect x="6" y="12" width="1" height="1"/><rect x="7" y="12" width="1" height="1"/><rect x="8" y="12" width="1" height="1"/><rect x="9" y="12" width="1" height="1"/><rect x="10" y="12" width="1" height="1"/><rect x="13" y="12" width="1" height="1"/><rect x="14" y="12" width="1" height="1"/><rect x="15" y="12" width="1" height="1"/><rect x="16" y="12" width="1" height="1"/><rect x="17" y="12" width="1" height="1"/><rect x="20" y="12" width="1" height="1"/><rect x="9" y="13" width="1" height="1"/><rect x="10" y="13" width="1" height="1"/><rect x="11" y="13" width="1" height="1"/><rect x="12" y="13" width="1" height="1"/><rect x="14" y="13" width="1" height="1"/><rect x="15" y="13" width="1" height="1"/><rect x="18" y="13" width="1" height="1"/><rect x="20" y="13" width="1" height="1"/><rect x="12" y="14" width="1" height="1"/><rect x="13" y="14" width="1" height="1"/><rect x="14" y="14" width="1" height="1"/><rect x="18" y="14" width="1" height="1"/><rect x="19" y="14" width="1" height="1"/><rect x="13" y="15" width="1" height="1"/><rect x="15" y="15" width="1" height="1"/><rect x="16" y="15" width="1" height="1"/><rect x="17" y="15" width="1" height="1"/><rect x="18" y="15" width="1" height="1"/><rect x="19" y="15" width="1" height="1"/><rect x="9" y="16" width="1" height="1"/><rect x="13" y="16" width="1" height="1"/><rect x="14" y="16" width="1" height="1"/><rect x="15" y="16" width="1" height="1"/><rect x="16" y="16" width="1" height="1"/><rect x="17" y="16" width="1" height="1"/><rect x="8" y="17" width="1" height="1"/><rect x="11" y="17" width="1" height="1"/><rect x="16" y="17" width="1" height="1"/><rect x="17" y="17" width="1" height="1"/><rect x="19" y="17" width="1" height="1"/><rect x="9" y="18" width="1" height="1"/><rect x="10" y="18" width="1" height="1"/><rect x="13" y="18" width="1" height="1"/><rect x="14" y="18" width="1" height="1"/><rect x="15" y="18" width="1" height="1"/><rect x="18" y="18" width="1" height="1"/><rect x="9" y="19" width="1" height="1"/><rect x="11" y="19" width="1" height="1"/><rect x="12" y="19" width="1" height="1"/><rect x="17" y="19" width="1" height="1"/><rect x="20" y="19" width="1" height="1"/><rect x="8" y="20" width="1" height="1"/><rect x="9" y="20" width="1" height="1"/><rect x="10" y="20" width="1" height="1"/><rect x="12" y="20" width="1" height="1"/><rect x="13" y="20" width="1" height="1"/><rect x="14" y="20" width="1" height="1"/><rect x="16" y="20" width="1" height="1"/><rect x="17" y="20" width="1" height="1"/><rect x="20" y="20" width="1" height="1"/></svg>
```
