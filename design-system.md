# Pacific IT Services — Design System

Derived directly from the submitted brand assets (`pacificit-fav-icon.svg`,
`vector-logo-pacificit.svg`). This supersedes the ad hoc dark/cyan theme
used in earlier carousels — that was pulled from the quote-tool web app's
UI, not the actual brand mark. This file is the authoritative palette
going forward.

## Logo mark

Both files draw the same abstract mark — a navy vertical bar alongside a
cluster of three overlapping circles (green, red, blue), the circles
decreasing in size:

- **Favicon** (`pacificit-fav-icon.svg`, 316×316): the mark sits inside a
  white rounded-square container (~10% corner radius) — use this version
  as an app icon, avatar, or anywhere the mark needs its own contained
  background (including on dark surfaces).
- **Full mark** (`vector-logo-pacificit.svg`, 500×500): the same shapes
  with no container, taller aspect ratio — use this version wherever you
  control the surrounding background yourself.

```svg
<!-- Full mark (vector-logo-pacificit.svg) -->
<svg width="500" height="500" viewBox="0 0 500 500" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0 35.8691H178.261V500H0V35.8691Z" fill="#22293E"/>
<path d="M446.738 223.369C446.738 326.923 366.684 410.869 267.933 410.869C169.182 410.869 89.1289 326.923 89.1289 223.369C89.1289 119.816 169.182 35.8691 267.933 35.8691C366.684 35.8691 446.738 119.816 446.738 223.369Z" fill="#5CA474"/>
<path d="M499.999 89.1304C499.999 138.356 460.094 178.261 410.869 178.261C361.643 178.261 321.738 138.356 321.738 89.1304C321.738 39.9051 361.643 0 410.869 0C460.094 0 499.999 39.9051 499.999 89.1304Z" fill="#D64550"/>
<path d="M445.654 454.891C445.654 479.203 425.701 498.913 401.089 498.913C376.476 498.913 356.523 479.203 356.523 454.891C356.523 430.578 376.476 410.869 401.089 410.869C425.701 410.869 445.654 430.578 445.654 454.891Z" fill="#6C91BF"/>
</svg>
```

```svg
<!-- Favicon / app-icon mark (pacificit-fav-icon.svg) -->
<svg width="316" height="316" viewBox="0 0 316 316" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0 31.5133C0 14.109 14.109 0 31.5133 0H283.619C301.024 0 315.133 14.109 315.133 31.5133V283.619C315.133 301.024 301.024 315.133 283.619 315.133H31.5133C14.109 315.133 0 301.024 0 283.619V31.5133Z" fill="white"/>
<path d="M72.7227 84.8438H133.325V242.41H72.7227V84.8438Z" fill="#22293E"/>
<path d="M224.228 148.476C224.228 183.62 197.096 212.109 163.626 212.109C130.156 212.109 103.023 183.62 103.023 148.476C103.023 113.333 130.156 84.8438 163.626 84.8438C197.096 84.8438 224.228 113.333 224.228 148.476Z" fill="#5CA474"/>
<path d="M242.411 103.024C242.411 119.759 228.845 133.325 212.11 133.325C195.375 133.325 181.809 119.759 181.809 103.024C181.809 86.289 195.375 72.7227 212.11 72.7227C228.845 72.7227 242.411 86.289 242.411 103.024Z" fill="#D64550"/>
<path d="M223.926 227.107C223.926 235.392 217.21 242.107 208.926 242.107C200.642 242.107 193.926 235.392 193.926 227.107C193.926 218.823 200.642 212.107 208.926 212.107C217.21 212.107 223.926 218.823 223.926 227.107Z" fill="#6C91BF"/>
</svg>
```

### Usage rules

- **Never recolor** the mark's shapes — the navy bar + green/red/blue
  circle cluster is fixed. Don't reduce it to a single accent color.
- **Clear space**: leave at least the width of the navy bar empty on
  every side.
- **Minimum size**: don't render the mark below ~64px on screen (the
  three circle sizes stop reading distinctly below that) or ~24px as a
  favicon/avatar.
- **Backgrounds**: the full mark (no container) needs a clean, mostly
  neutral background — white or Navy 900 (`#22293E`) both work; avoid
  busy photography or mid-tone colors behind it. On any other dark
  surface, use the favicon's white-boxed version instead of placing the
  bare mark directly on the color.
- No wordmark/logotype ships in either file — "Pacific IT Services" is
  set as text (see Typography), not part of the mark.

## Color palette

| Role | Name | Hex | Use for |
|---|---|---|---|
| Primary / text | Navy | `#22293E` | Headlines, body copy, dark surfaces, the logo's bar |
| Primary accent | Green | `#5CA474` | CTAs, highlights, the dominant accent — use most often after navy/white |
| Secondary accent | Red | `#D64550` | Sparing use — a single highlighted detail, never body text or large fills |
| Tertiary accent | Blue | `#6C91BF` | Sparing use — a second small accent alongside green, not a replacement for it |
| Background | White | `#FFFFFF` | Default background — this is a light-brand, not a dark one |

Usage weight should roughly mirror the logo itself: navy and white carry
the composition, green is the one accent used generously, red and blue
are small, occasional details (exactly as they appear in the mark — big
green circle, smaller red, smallest blue).

Suggested tonal variants for UI work (derived, not from source files —
adjust if a real token set exists elsewhere):

| Token | Hex | Use for |
|---|---|---|
| Navy 900 (base) | `#22293E` | As above |
| Navy 700 | `#3A4360` | Hover/lighter navy surface |
| Off-white surface | `#F5F6F1` | Card backgrounds on a white page (matches the light-theme carousel already built) |
| Border | `#E1E3DA` | Hairlines / dividers on white |
| Muted text | `#6B7080` | Captions, labels, secondary copy |
| Green 700 (text-safe) | `#3B7A51` | Green **text** on white or off-white: eyebrows, links, small labels |

### Contrast rules (WCAG AA)

Brand Green `#5CA474` is a mid-tone. It works as a fill or a graphic,
but it is too light to carry white text, and too light to be used as
small text on white. Use these pairings:

| Pairing | Ratio | Status | Use |
|---|---|---|---|
| Navy `#22293E` on White | 14.4:1 | Pass | Headlines, body copy |
| White on Navy `#22293E` | 14.4:1 | Pass | Text on dark surfaces |
| **Navy `#22293E` on Green `#5CA474`** | **4.8:1** | **Pass** | **CTA buttons (default)** |
| Green 700 `#3B7A51` on White | 5.1:1 | Pass | Green text: eyebrows, links, labels |
| Green 700 `#3B7A51` on Off-white `#F5F6F1` | 4.7:1 | Pass | Green text on cards |
| Muted `#6B7080` on White | 4.9:1 | Pass | Captions, secondary copy |
| White on Green `#5CA474` | 3.0:1 | **Fail** | Don't use for button or body text |
| Green `#5CA474` on White (as text) | 3.0:1 | **Fail** | Only for text 24px+ bold, icons and graphics |
| Blue `#6C91BF` on White (as text) | 3.3:1 | **Fail** | Graphics and accents only, never text |

AA requires 4.5:1 for normal text and 3:1 for large text (24px+, or
18.66px+ bold) and UI graphics.

## Typography

No typeface ships with the logo files. **Inter** (Google Fonts) is
carried over from the existing web app and prior carousels as the
working default — geometric, highly legible, pairs cleanly with the
mark's circular geometry. Replace this section if a real brand type
spec exists elsewhere.

- Headlines: Inter, weight 800, tight letter-spacing (-1 to -1.5px)
- Body: Inter, weight 400–500
- Labels / eyebrows: Inter, weight 700, uppercase, wide letter-spacing (3–4px)

## Applying this to social carousels

- Default to a **white/off-white background**, not dark — this matches
  the logo's own container and is a deliberate change from earlier
  carousels built before these assets existed.
- Header on every slide: the full mark (small, ~32–40px) + "PACIFIC IT
  SERVICES" wordmark in Navy, bold, uppercase, tracked out.
- Primary accent for checkmarks, progress dots and CTA button fills:
  **Green** `#5CA474`. When the accent is small text (eyebrows, links,
  labels), use **Green 700** `#3B7A51` so it stays readable.
- Reserve **Red** and **Blue** for small highlighted details only (a
  single callout, a per-item accent in a comparison slide) — never as
  the dominant color of a slide.
- CTA buttons: **Green `#5CA474` fill with Navy `#22293E` text**
  (4.8:1, passes AA). Don't use white text on green (3.0:1, fails).
  Secondary option: Navy fill with white text (14.4:1).
