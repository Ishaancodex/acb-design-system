# ANACITY Business — Design System

A comprehensive dark-mode design language for the **Dev ACB Visitor Management Platform**. Built for OLED displays, mobile-first layouts, and accessible contrast ratios. Delivered as a single self-contained HTML file — no build tools or dependencies required.

---

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [File Structure](#file-structure)
- [Design Principles](#design-principles)
- [Color System](#color-system)
- [Typography](#typography)
- [Spacing](#spacing)
- [Components](#components)
- [Screen Gallery](#screen-gallery)
- [Design Tokens](#design-tokens)
- [Interactive Features](#interactive-features)
- [Browser Support](#browser-support)

---

## Overview

The Dev ACB Design System provides a shared visual language for designers and developers building the visitor management platform. It documents every colour token, typographic style, spacing value, and UI component used across the product's 80+ screens.

| Property | Value |
|---|---|
| Theme | Dark Mode (OLED-optimised) |
| Primary Font | Readex Pro |
| Monospace Font | DM Mono |
| Primary Colour | Gold Gradient (`#FFD09B → #B0814D`) |
| Accent Colour | Purple (`#663879`) |
| Base Grid | 4px |

---

## Getting Started

The design system is a single HTML file. Open it directly in any modern browser — no server, no build step, no dependencies.

```bash
# Clone or download the file, then open it
open index.html
```

All fonts are loaded from Google Fonts via CDN. An internet connection is required for fonts to render correctly.

---

## File Structure

```
index.html          # Complete design system — styles, markup, and JS in one file
README.md           # This file
```

The HTML file is organised into six sections, each accessible via the sticky navigation bar:

| # | Section | Description |
|---|---|---|
| 01 | Colors | Full colour palette with copyable hex values |
| 02 | Typography | Font families and type scale |
| 03 | Spacing | 4px grid scale and usage examples |
| 04 | Components | Interactive UI components |
| 05 | Screen Gallery | Thumbnail previews of key app screens |
| 06 | Tokens | Complete CSS custom properties reference |

---

## Design Principles

**Dark-first.** Every colour is chosen for dark backgrounds. Background values are layered — screen (`#121212`), card (`#1D1D1D`), selectable (`#2B2B2B`) — creating depth without harsh contrast.

**Gold as primary.** The gold gradient (`#FFD09B → #B0814D`) is the most prominent action colour: buttons, active states, highlights, and interactive feedback. Purple (`#663879`) is reserved for accents and structural highlights.

**4px grid.** All spacing is a multiple of 4px, from the smallest gap (`4px / xs`) to the largest section padding (`32px / xxl`).

**Mobile-first.** Touch targets, card sizes, and type scales are sized for mobile screens first and scale up gracefully.

---

## Color System

### Background Colors

| Name | Token | Hex |
|---|---|---|
| Screen Background | `--color-bg-screen` | `#121212` |
| Card Background | `--color-bg-card` | `#1D1D1D` |
| Selectable BG | `--color-bg-selectable` | `#2B2B2B` |

### Text Colors

| Name | Token | Hex |
|---|---|---|
| Text Primary | `--color-text-primary` | `#EBEBEB` |
| Text Secondary | `--color-text-secondary` | `#DBDBDB` |
| Text Tertiary | `--color-text-tertiary` | `#ADADAD` |
| Text Disabled | `--color-text-disabled` | `#868686` |

### Brand Colors

| Name | Token | Hex | Usage |
|---|---|---|---|
| Gold Primary | `--color-brand-gold` | `#FFD09B → #B0814D` | Primary actions, highlights |
| Purple Accent | `--color-brand-purple` | `#663879` | Accents, structural elements |
| Gold Dark | `--color-brand-gradient-bottom` | `#B0814D` | Gradient end, deep gold states |

### Semantic Colors

| Name | Token | Hex | Usage |
|---|---|---|---|
| Success | `--color-success` | `#5FD796` | Approved, confirmed, active |
| Error | `--color-error` | `#EA7C7C` | Declined, failed, invalid |
| Info | `--color-info` | `#71B4FF` | Informational states, inside |
| Warning | `--color-warning` | `#FFB347` | Pending, caution states |
| Error Background | `--color-bg-error` | `#290000` | Error container backgrounds |

---

## Typography

Both fonts are loaded from [Google Fonts](https://fonts.google.com).

### Font Families

| Role | Family | Token |
|---|---|---|
| Primary (Headings & UI) | Readex Pro | `--font-primary` |
| Secondary (Body text) | Readex Pro | `--font-secondary` |
| Monospace (Code & tokens) | DM Mono | `--font-mono` |

### Type Scale

| Style | Size | Weight | Line Height | Letter Spacing | Usage |
|---|---|---|---|---|---|
| h5-Medium | 16px | 500 | 20px | 0px | Section headings |
| h7-Semibold | 12px | 600 | 16px | 0px | Labels & tags |
| h8-Medium | 10px | 500 | 14px | 0px | Small labels |
| p3-Regular | 12px | 400 | 16px | 0px | Body text small |
| Body 1 | 14px | 400 | 20px | +0.16px | Primary body text |
| Body 2 | 13px | 500 | 24px | +0.16px | Secondary body |

---

## Spacing

All spacing values are multiples of the 4px base unit.

| Token | Value | Common Usage |
|---|---|---|
| `--spacing-xs` | 4px | Icon gaps, tight inline spacing |
| `--spacing-sm` | 8px | Between related elements |
| `--spacing-md` | 12px | Component internal gaps |
| `--spacing-lg` | 16px | Card padding, screen padding |
| `--spacing-xl` | 24px | Section gaps, large component padding |
| `--spacing-xxl` | 32px | Between major layout sections |

### Border Radius

| Token | Value | Usage |
|---|---|---|
| `--radius-sm` | 8px | Buttons, inputs, small cards |
| `--radius-md` | 12px | Standard cards, modals |
| `--radius-lg` | 16px | Large cards, containers |
| `--radius-full` | 9999px | Pills, badges, avatars |

---

## Components

All components in the design system are fully interactive in the browser.

### Buttons

| Variant | Class | Usage |
|---|---|---|
| Primary | `.btn--primary` | Main CTA — gold gradient background |
| Secondary | `.btn--secondary` | Secondary actions |
| Ghost | `.btn--ghost` | Tertiary, low-emphasis actions |
| Icon | `.btn--icon` | Icon-only actions |
| FAB | `.btn--fab` | Floating action button — gold gradient |
| Success | `.btn--success` | Approve / confirm actions |
| Error | `.btn--error` | Decline / destructive actions |
| Small | `.btn--small` | Compact button variant, combinable |

```html
<!-- Primary button -->
<button class="btn btn--primary">Approve Visit</button>

<!-- Small ghost button -->
<button class="btn btn--small btn--ghost">Cancel</button>
```

### Input Fields

| Variant | Class | Usage |
|---|---|---|
| Text input | `.input` | Standard text entry |
| Search input | `.input--with-icon` | Search with leading icon |
| Dropdown | `.dropdown` | Select from a list of options |

Focus states use a gold border and gold glow ring.

### Cards

| Variant | Class | Usage |
|---|---|---|
| Standard card | `.card` | Visit details, content containers |
| Contact card | `.card--contact` | Visitor contact row with avatar |

Card sub-elements: `.card__header`, `.card__title`, `.card__content`, `.card__text`, `.card__meta`, `.card__actions`, `.card__badge`.

### Status Badges

| Variant | Class | Colour |
|---|---|---|
| Upcoming | `.badge--success` | Green `#5FD796` |
| Inside | `.badge--info` | Blue `#71B4FF` |
| Pending | `.badge--warning` | Amber `#FFB347` |
| Declined | `.badge--error` | Red `#EA7C7C` |
| Past | `.badge--neutral` | Grey |

```html
<span class="badge badge--success">Upcoming</span>
<span class="badge badge--error">Declined</span>
```

### Data Display

Key–value rows for displaying visitor details. Uses `.data-row`, `.data-row__label`, `.data-row__value`. Add `.data-row__value--success` for green success values.

### Checkbox

Custom-styled checkbox with gold gradient checked state. Supports checked, unchecked, and disabled states.

```html
<label class="checkbox">
  <input type="checkbox" checked>
  <span class="checkbox__box"></span>
  <span class="checkbox__label">Agree to terms</span>
</label>
```

### Calendar

Interactive month calendar. Navigate months with the arrow buttons. Clicking a date selects it and shows a toast confirmation. Today's date is highlighted in gold.

---

## Screen Gallery

Thumbnail previews covering the three main flow categories:

**Home & Dashboard**
- Home — main dashboard view
- View All — full visitor list
- Activity — recent activity log

**Add Visitor Flows**
- Add Guest — visitor entry form
- Calendar — date picker screen
- Time Slot — time selection

**Pass Management**
- Digital Pass — QR/barcode pass view
- Approved — confirmed pass state
- Declined — rejected pass state

---

## Design Tokens

All design decisions are encoded as CSS custom properties on `:root`. Copy the full token set from the **Tokens** section of the design system page, or use the values below:

```css
:root {
  /* Colors */
  --color-bg-screen:     #121212;
  --color-bg-card:       #1D1D1D;
  --color-bg-selectable: #2B2B2B;
  --color-text-primary:  #EBEBEB;
  --color-text-secondary:#DBDBDB;
  --color-text-tertiary: #ADADAD;
  --color-text-disabled: #868686;
  --color-brand-gold:    #FFD09B;
  --color-brand-purple:  #663879;
  --color-success:       #5FD796;
  --color-error:         #EA7C7C;
  --color-info:          #71B4FF;
  --color-bg-error:      #290000;

  /* Typography */
  --font-primary:   'Readex Pro', sans-serif;
  --font-secondary: 'Readex Pro', sans-serif;
  --font-mono:      'DM Mono', monospace;

  /* Spacing */
  --spacing-xs:  4px;
  --spacing-sm:  8px;
  --spacing-md:  12px;
  --spacing-lg:  16px;
  --spacing-xl:  24px;
  --spacing-xxl: 32px;

  /* Border Radius */
  --radius-sm:   8px;
  --radius-md:   12px;
  --radius-lg:   16px;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-card:     0 2px 16px rgba(0, 0, 0, 0.4);
  --shadow-selected: inset 0 0 10px #FFBF76;
}
```

---

## Interactive Features

The design system page includes several interactive behaviours intended to make it practical for both designers and developers:

- **Click any colour card** to copy its hex value to the clipboard. A toast notification confirms the copy.
- **Copy CSS button** in the Tokens section copies the entire `:root` token block.
- **Calendar** is fully navigable — use the arrow buttons to move between months, and click any date to select it.
- **Dropdown** opens a styled menu with selectable visitor type options.
- **Buttons** have hover, active, and disabled states visible on interaction.
- **Checkboxes** toggle between checked and unchecked with animated transitions.
- **Active nav link** updates automatically as you scroll through sections.

---

## Browser Support

| Browser | Support |
|---|---|
| Chrome / Edge 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Mobile Chrome / Safari | ✅ Full support |

Requires an internet connection to load Readex Pro and DM Mono from Google Fonts. Font fallback is `sans-serif` / `monospace`.

---

*Dev ACB Design System — Visitor Management Platform*
