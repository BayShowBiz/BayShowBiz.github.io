<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>BayShowBiz Business Card - Front & Back</title>
<meta name="viewport" content="width=device-width, initial-scale=1" />

<style>
:root {
--color-bg: #f7f4ee;
--color-surface: #ffffff;
--color-primary: #c95c2a;
--color-primary-dark: #9b4115;
--color-accent: #f3b32c;
--color-text: #222222;
--color-muted: #666666;
--shadow-soft: 0 10px 25px rgba(0, 0, 0, 0.15);
--radius-lg: 14px;
--radius-pill: 999px;
}

* {
box-sizing: border-box;
margin: 0;
padding: 0;
}

body {
min-height: 100vh;
font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
background: radial-gradient(circle at top, #ffe9c4, #f7f4ee 45%, #e8e2d6);
display: flex;
align-items: center;
justify-content: center;
padding: 1.5rem;
}

.page-wrapper {
display: grid;
grid-template-columns: repeat(2, auto);
gap: 1.8rem;
}

.card-wrapper {
display: grid;
gap: 0.4rem;
justify-items: center;
}

.card-label {
font-size: 0.8rem;
text-transform: uppercase;
letter-spacing: 0.14em;
color: var(--color-muted);
}

/* Business card base */
.card {
width: 340px; /* close to 3.5" visual size */
aspect-ratio: 3.5 / 2; /* standard card proportion */
background: var(--color-surface);
border-radius: var(--radius-lg);
box-shadow: var(--shadow-soft);
padding: 1rem 1.2rem;
position: relative;
overflow: hidden;
display: grid;
}

.card::before {
content: "";
position: absolute;
inset: -40%;
background:
radial-gradient(circle at 0 0, #ffecc1, transparent 55%),
radial-gradient(circle at 100% 0, #ffb38c, transparent 55%),
radial-gradient(circle at 0 100%, #ffd2e2, transparent 55%);
opacity: 0.22;
pointer-events: none;
}

.card-inner {
position: relative;
z-index: 1;
height: 100%;
display: grid;
}

/* FRONT SIDE */

.card-front-inner {
grid-template-rows: auto 1fr auto;
gap: 0.5rem;
}

.logo-row {
display: flex;
align-items: center;
justify-content: space-between;
gap: 0.5rem;
}

.logo-left {
display: flex;
align-items: center;
gap: 0.4rem;
}

.logo-mark {
width: 30px;
height: 30px;
border-radius: 50%;
background: radial-gradient(circle at 30% 30%, #ffe9a8, #f07f3c);
display: flex;
align-items: center;
justify-content: center;
font-weight: 900;
font-size: 0.9rem;
color: #fff;
box-shadow: 0 6px 14px rgba(0, 0, 0, 0.22);
}

.logo-text-main {
font-weight: 800;
letter-spacing: 0.07em;
text-transform: uppercase;
font-size: 0.8rem;
}

.logo-text-sub {
font-size: 0.62rem;
text-transform: uppercase;
letter-spacing: 0.16em;
color: var(--color-muted);
}

.tag-pill {
font-size: 0.62rem;
padding: 0.2rem 0.6rem;
border-radius: var(--radius-pill);
border: 1px solid rgba(0, 0, 0, 0.06);
background: rgba(255, 255, 255, 0.85);
text-transform: uppercase;
letter-spacing: 0.14em;
white-space: nowrap;
}

.middle-front {
display: grid;
align-content: center;
gap: 0.25rem;
}

.name {
font-size: 1.1rem;
font-weight: 700;
letter-spacing: 0.04em;
}

.role {
font-size: 0.78rem;
text-transform: uppercase;
letter-spacing: 0.16em;
color: var(--color-muted);
}

.divider {
width: 52%;
height: 3px;
border-radius: 999px;
margin-top: 0.3rem;
background: linear-gradient(90deg, var(--color-primary), var(--color-accent));
}

.tagline {
font-size: 0.74rem;
color: var(--color-muted);
margin-top: 0.3rem;
}

.bottom-front {
display: flex;
justify-content: space-between;
align-items: center;
gap: 0.6rem;
font-size: 0.72rem;
color: var(--color-text);
flex-wrap: wrap;
}

.website {
font-weight: 600;
color: var(--color-primary-dark);
}

.handle {
font-size: 0.72rem;
color: var(--color-muted);
}

/* BACK SIDE */

.card-back-inner {
grid-template-rows: auto 1fr auto;
gap: 0.4rem;
font-size: 0.74rem;
color: var(--color-text);
}

.back-header {
display: flex;
justify-content: space-between;
align-items: center;
gap: 0.5rem;
}

.back-title {
text-transform: uppercase;
letter-spacing: 0.16em;
font-size: 0.7rem;
color: var(--color-muted);
}

.back-tagline {
font-size: 0.76rem;
font-weight: 600;
color: var(--color-primary-dark);
}

.shows-list {
margin-top: 0.2rem;
display: grid;
gap: 0.25rem;
}

.show-line {
display: flex;
align-items: flex-start;
gap: 0.35rem;
}

.show-dot {
width: 6px;
height: 6px;
border-radius: 50%;
margin-top: 0.23rem;
background: var(--color-primary);
}

.show-text-title {
font-weight: 600;
font-size: 0.76rem;
}

.show-text-sub {
font-size: 0.72rem;
color: var(--color-muted);
}

.back-bottom {
display: flex;
justify-content: space-between;
align-items: flex-end;
gap: 0.6rem;
flex-wrap: wrap;
margin-top: 0.2rem;
}

.back-contact-block {
display: grid;
gap: 0.1rem;
}

.back-label {
font-size: 0.62rem;
text-transform: uppercase;
letter-spacing: 0.16em;
color: var(--color-muted);
}

.back-line {
display: flex;
align-items: center;
gap: 0.25rem;
font-size: 0.72rem;
}

.back-line span {
white-space: nowrap;
}

.rate-pill {
padding: 0.18rem 0.55rem;
border-radius: var(--radius-pill);
border: 1px solid rgba(0, 0, 0, 0.08);
font-size: 0.7rem;
background: rgba(255, 255, 255, 0.9);
}

.qr-placeholder {
padding: 0.4rem 0.55rem;
border-radius: var(--radius-md, 8px);
border: 1px dashed rgba(0, 0, 0, 0.2);
font-size: 0.7rem;
max-width: 120px;
text-align: center;
background: rgba(255, 255, 255, 0.8);
}

@media (max-width: 800px) {
.page-wrapper {
grid-template-columns: 1fr;
}
body {
padding: 1rem;
}
}

@media print {
body {
background: #ffffff;
padding: 0.5rem;
}

.page-wrapper {
gap: 1rem;
}

.card {
box-shadow: none;
}

.card-label {
display: none; /* hide "Front"/"Back" labels if you just want the cards */
}
}
</style>
</head>
<body>

<div class="page-wrapper">

<!-- FRONT -->
<div class="card-wrapper">
<div class="card-label">Front</div>
<div class="card">
<div class="card-inner card-front-inner">
<!-- Top -->
<div class="logo-row">
<div class="logo-left">
<div class="logo-mark">B</div>
<div>
<div class="logo-text-main">BayShowBiz</div>
<div class="logo-text-sub">Live music & joy for seniors</div>
</div>
</div>
<div class="tag-pill">Bay Area • CA</div>
</div>

<!-- Middle -->
<div class="middle-front">
<div class="name">Colinda De Groen</div>
<div class="role">Musician & Senior Entertainment</div>
<div class="divider"></div>
<div class="tagline">
Interactive sing-alongs, lights &amp; music for senior communities.
</div>
</div>

<!-- Bottom -->
<div class="bottom-front">
<div>
<div class="website">BayShowBiz.com</div>
</div>
<div class="handle">@BayShowBiz • Los Altos, CA</div>
</div>
</div>
</div>
</div>

<!-- BACK -->
<div class="card-wrapper">
<div class="card-label">Back</div>
<div class="card">
<div class="card-inner card-back-inner">
<!-- Header -->
<div class="back-header">
<div>
<div class="back-title">Show highlights</div>
<div class="back-tagline">3 uplifting options for your residents</div>
</div>
<div class="rate-pill">$150 / hour • Own sound system</div>
</div>

<!-- Shows list -->
<div class="shows-list">
<div class="show-line">
<div class="show-dot"></div>
<div>
<div class="show-text-title">Live Instrument Sing-Along</div>
<div class="show-text-sub">
Upbeat sing-alongs with multiple instruments and classics from the 40s–80s.
</div>
</div>
</div>

<div class="show-line">
<div class="show-dot"></div>
<div>
<div class="show-text-title">Music, Lights &amp; Dancing</div>
<div class="show-text-sub">
Light-up outfits, soundtracks, and movement-friendly fun for parties &amp; events.
</div>
</div>
</div>

<div class="show-line">
<div class="show-dot"></div>
<div>
<div class="show-text-title">Private Room Visits</div>
<div class="show-text-sub">
Gentle ukulele visits and soft songs for residents who stay in their rooms.
</div>
</div>
</div>
</div>

<!-- Bottom contact -->
<div class="back-bottom">
<div class="back-contact-block">
<div class="back-label">Booking</div>
<div class="back-line">
<span>(720) 882-1677</span>
</div>
<div class="back-line">
<span>bayshowbiz@icloud.com</span>
</div>
<div class="back-line">
<span>Los Altos, CA • Bay Area</span>
</div>
</div>

<div class="back-contact-block">
<div class="back-label">Videos</div>
<div class="back-line">
<span>YouTube.com/@BayShowBiz</span>
</div>
<div class="qr-placeholder">
Optional: add QR code<br />
to your website or YouTube.
</div>
</div>
</div>

</div>
</div>
</div>

</div>

</body>
</html>
