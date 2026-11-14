# Pacific IT Services — Design System

The brand rules for **Pacific IT Services**, a web development and marketing
business serving local Ontario businesses ([pacificit.cloud](https://pacificit.cloud)).
Use this repo as the single source of truth for any Pacific IT design:
websites, pitch decks, one-pagers, proposals, Instagram carousels and video.

The full spec lives in **[`design-system.md`](design-system.md)**. This page is
the quick reference.

## What's in this repo

| File | What it is |
|---|---|
| [`design-system.md`](design-system.md) | The full spec: logo rules, palette, contrast rules, typography and social carousel guidance |
| [`vector-logo-pacificit.svg`](vector-logo-pacificit.svg) | Full logo mark (500×500), no background. Use it on white or navy. |
| [`pacificit-fav-icon.svg`](pacificit-fav-icon.svg) | The mark inside a white rounded square (316×316). Use it for favicons, avatars, app icons and any dark or coloured background. |

## Logo

The mark is a navy vertical bar beside three overlapping circles in green,
red and blue. There is no wordmark file, so "PACIFIC IT SERVICES" is set in
Inter next to the mark.

- Never recolour, stretch or rearrange the mark.
- Leave clear space at least the width of the navy bar on every side.
- Minimum size is about 64px on screen, or 24px as a favicon.
- Put the bare mark only on white or navy. On anything else, use the boxed favicon version.

## Colours

| Role | Name | Hex |
|---|---|---|
| Text, dark surfaces | Navy | `#22293E` |
| Main accent, CTA fills | Green | `#5CA474` |
| Green text (eyebrows, links) | Green 700 | `#3B7A51` |
| Small highlight only | Red | `#D64550` |
| Small highlight only | Blue | `#6C91BF` |
| Background | White | `#FFFFFF` |
| Card surface | Off-white | `#F5F6F1` |
| Hover or lighter navy | Navy 700 | `#3A4360` |
| Dividers | Border | `#E1E3DA` |
| Captions, secondary copy | Muted | `#6B7080` |

Pacific IT is a **light brand**. Navy and white carry the design, green is
the one accent used generously, and red and blue appear only as small
details, in the same proportions as the logo.

> The older dark theme (cyan `#00BCD4` on `#0A0A0A`) came from the quote
> tool's UI, not the brand. Don't use it for new work.

## Contrast: the rules that matter

- **CTA buttons: Green fill with Navy text** (4.8:1). Never white text on green (3.0:1, fails WCAG AA).
- **Green as text:** use Green 700 `#3B7A51`. Brand Green is too light for small text on white.
- **Blue and red** are for graphics and accents, not body text.

The full contrast table is in [`design-system.md`](design-system.md#contrast-rules-wcag-aa).

## Typography

**Inter** (Google Fonts) for everything.

| Style | Weight | Notes |
|---|---|---|
| Headlines | 800 | Tight letter-spacing (-1 to -1.5px) |
| Body | 400–500 | |
| Labels and eyebrows | 700 | Uppercase, letter-spacing 3–4px |

## CSS tokens

Paste this into any web project to start on-brand:

```css
:root {
  --pit-navy: #22293E;
  --pit-navy-700: #3A4360;
  --pit-green: #5CA474;
  --pit-green-700: #3B7A51; /* green text */
  --pit-red: #D64550;
  --pit-blue: #6C91BF;
  --pit-white: #FFFFFF;
  --pit-surface: #F5F6F1;
  --pit-border: #E1E3DA;
  --pit-muted: #6B7080;
  --pit-font: "Inter", system-ui, sans-serif;
}

.pit-button {
  background: var(--pit-green);
  color: var(--pit-navy); /* not white: white on green fails contrast */
  font: 700 16px/1 var(--pit-font);
  padding: 14px 24px;
  border-radius: 8px;
}
```

## Using it with Claude

Point Claude at this repo, or paste `design-system.md`, and ask it to follow
the Pacific IT design system. That works for decks, one-pagers, carousels
and Remotion videos.
