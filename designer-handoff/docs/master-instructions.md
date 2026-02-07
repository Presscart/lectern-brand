# Lectern Visual Identity — Master Instructions

## Brand Colors

| Name  | Hex       | Usage |
|-------|-----------|-------|
| Ink   | `#1a1612` | Primary dark. Backgrounds, text, contained icon fill. |
| Gilt  | `#f9f6ec` | Primary light. Backgrounds, text on dark, gold-tinted warmth. |
| Brass | `#c9a961` | Accent. Icon gradient, CTAs, highlights, premium touches. |

---

## Logo Versions

### 1. Uncontained (Primary Logo)
- Three horizontal bars only, no container
- **This is the primary logo** — use in most contexts
- ViewBox: `22 30 48 35`
- Always uses **20% → 100% opacity gradient** (left to right)
- **Brass icon versions are primary**; monochrome (Ink/Gilt) available for single-color contexts

### 2. Contained (Selective Use)
- Three horizontal bars inside a rounded square container
- **Use for:** Favicons, profile photos, app icons, and other square contexts
- Container has `rx="18"` corner radius
- ViewBox: `0 0 100 100`
- Always uses **20% → 100% opacity gradient** on the bars

---

## Vertical Alignment Rules

### CRITICAL: Icon-to-Wordmark Alignment

**Uncontained Icon:**
- The **top of the top bar** must align with the **top of the "L"** in the wordmark
- The **bottom of the bottom bar** must align with the **bottom of the "L"** in the wordmark
- This means the icon height equals the cap height of the wordmark

**Contained Icon:**
- The **top of the container** must align with the **top of the "L"** in the wordmark
- The **bottom of the container** must align with the **bottom of the "L"** in the wordmark
- This means the container height equals the cap height of the wordmark

---

## Lockup Spacing

- Gap between **uncontained icon** and wordmark: **10px**
- Gap between **contained icon** and wordmark: **12px**
- Icon and wordmark are **vertically centered** to each other

---

## Color Pairing Rules

**CRITICAL: Never place same-tone elements on same-tone backgrounds.**

| Background | Icon Color | Wordmark Color |
|------------|------------|----------------|
| Ink        | Gilt or Brass gradient | Gilt |
| Gilt       | Ink or Brass gradient  | Ink  |

### Primary Combinations (Brass Icon)
1. **Brass on Ink** — Primary dark lockup (brass gradient icon + gilt wordmark on ink background)
2. **Brass on Gilt** — Primary light lockup (brass gradient icon + ink wordmark on gilt background)

### Monochrome Alternatives
3. **Gilt on Ink** — Monochrome dark (gilt gradient icon + gilt wordmark on ink background)
4. **Ink on Gilt** — Monochrome light (ink gradient icon + ink wordmark on gilt background)

### Contained Icon (App Icon)
The contained icon uses contrasting container colors with brass gradient bars:
- **On Gilt background:** Ink container (#1a1612) + Brass gradient bars
- **On Ink background:** Gilt container (#f9f6ec) + Brass gradient bars

The container must always contrast with the page background for visibility.

### Never Do
- Ink icon on Ink background
- Gilt icon on Gilt background
- Any same-color pairing that lacks contrast

---

## Opacity Gradient Specification

**All icon bars must use the opacity gradient.** This is a defining characteristic of the Lectern brand.

- **Start (left):** 20% opacity
- **End (right):** 100% opacity
- Direction: `x1="0%" y1="0%" x2="100%" y2="0%"`

### SVG Gradient Template (Brass — Primary)
```svg
<linearGradient id="brass-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
  <stop offset="0%" stop-color="#c9a961" stop-opacity="0.2"/>
  <stop offset="100%" stop-color="#c9a961" stop-opacity="1"/>
</linearGradient>
```

### SVG Gradient Template (Gilt — For dark backgrounds)
```svg
<linearGradient id="gilt-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
  <stop offset="0%" stop-color="#f9f6ec" stop-opacity="0.2"/>
  <stop offset="100%" stop-color="#f9f6ec" stop-opacity="1"/>
</linearGradient>
```

### SVG Gradient Template (Ink — For light backgrounds)
```svg
<linearGradient id="ink-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
  <stop offset="0%" stop-color="#1a1612" stop-opacity="0.2"/>
  <stop offset="100%" stop-color="#1a1612" stop-opacity="1"/>
</linearGradient>
```

---

## Icon Sizing Rules

### Uncontained Icon
The icon height must equal the **cap height** of the wordmark "L".

| Font Size | Cap Height | Icon Width | Icon Height |
|-----------|------------|------------|-------------|
| 96px      | ~74px      | 95px       | 74px        |
| 72px      | ~55px      | 71px       | 55px        |
| 56px      | ~43px      | 55px       | 43px        |
| 42px      | ~32px      | 41px       | 32px        |
| 28px      | ~22px      | 28px       | 22px        |
| 22px      | ~17px      | 22px       | 17px        |

Cap height is approximately **77%** of font size for Fraunces.

### Contained Icon
When used in a lockup, the container height equals the cap height of the wordmark.
The container is square, so width = height.

| Font Size | Cap Height | Container Size |
|-----------|------------|----------------|
| 42px      | ~32px      | 42x42px        |
| 28px      | ~22px      | 28x28px        |

---

## Typography

### Wordmark Font
- **Typeface:** Fraunces (Google Fonts)
- **Primary Weight:** Medium (500)
- **Styles:** Roman only — no italics
- **Case:** Title case ("Lectern")

### Weight Usage
- **Light (300), Regular (400):** Not recommended for wordmark
- **Medium (500):** Primary wordmark weight
- **Semibold (600) through Black (900):** Available for emphasis, headlines, or alternate treatments

---

## Uncontained Icon SVG Template

```svg
<svg width="41" height="32" viewBox="22 30 48 35" fill="none" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="brass-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#c9a961" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#c9a961" stop-opacity="1"/>
    </linearGradient>
  </defs>
  <path d="M26,32.75 Q24,32.75 24,34.25 L24,35.25 Q24,37 26,37 L66,37 Q68,37 68,35 L68,32 Q68,30 66,30 L26,32.75 Z" fill="url(#brass-gradient)"/>
  <rect x="24" y="44" width="32" height="7" rx="2" fill="url(#brass-gradient)"/>
  <rect x="24" y="58" width="44" height="7" rx="2" fill="url(#brass-gradient)"/>
</svg>
```

---

## Contained Icon SVG Template (Ink Container — For Gilt backgrounds)

```svg
<svg width="42" height="42" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="brass-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#c9a961" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#c9a961" stop-opacity="1"/>
    </linearGradient>
  </defs>
  <rect x="8" y="8" width="84" height="84" rx="18" fill="#1a1612"/>
  <path d="M26,32.75 Q24,32.75 24,34.25 L24,35.25 Q24,37 26,37 L66,37 Q68,37 68,35 L68,32 Q68,30 66,30 L26,32.75 Z" fill="url(#brass-gradient)"/>
  <rect x="24" y="44" width="32" height="7" rx="2" fill="url(#brass-gradient)"/>
  <rect x="24" y="58" width="44" height="7" rx="2" fill="url(#brass-gradient)"/>
</svg>
```

---

## Contained Icon SVG Template (Gilt Container — For Ink backgrounds)

```svg
<svg width="42" height="42" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="brass-gradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#c9a961" stop-opacity="0.2"/>
      <stop offset="100%" stop-color="#c9a961" stop-opacity="1"/>
    </linearGradient>
  </defs>
  <rect x="8" y="8" width="84" height="84" rx="18" fill="#f9f6ec"/>
  <path d="M26,32.75 Q24,32.75 24,34.25 L24,35.25 Q24,37 26,37 L66,37 Q68,37 68,35 L68,32 Q68,30 66,30 L26,32.75 Z" fill="url(#brass-gradient)"/>
  <rect x="24" y="44" width="32" height="7" rx="2" fill="url(#brass-gradient)"/>
  <rect x="24" y="58" width="44" height="7" rx="2" fill="url(#brass-gradient)"/>
</svg>
```

---

## Quick Reference Checklist

When creating any brand asset:

- [ ] Using uncontained logo as primary (contained only for app icons, favicons, profile photos)
- [ ] Brass icon versions are primary; monochrome only for single-color contexts
- [ ] Icon uses 20% → 100% opacity gradient (ALWAYS)
- [ ] Icon/container aligns with cap height of wordmark "L" (top-to-top, bottom-to-bottom)
- [ ] Correct gap spacing (10px uncontained, 12px contained)
- [ ] Icon color contrasts with background (never same-tone on same-tone)
- [ ] Fraunces Medium (500) for wordmark
- [ ] Using correct viewBox (`22 30 48 35` uncontained, `0 0 100 100` contained)

---

## Reference Document

The complete visual identity showcase is available at:
`/logos/final/lectern-complete-brand-showcase.html`

This document serves as the brand visual identity bible and demonstrates all approved logo applications.
