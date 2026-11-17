---
name: swiss-international-style
description: Produce layouts, image prompts and specs in Swiss Style (International Typographic Style). Use when the user asks for Swiss style, International Typographic Style, Helvetica typography, 12-column grid posters, or "minimal + grid + oversized headline" layout design.
version: 0.2.0
---

# Swiss International Style Layout Design

Work strictly within the visual grammar of 1950s Swiss International Typographic Style.
Every output must comply with the rules below. **Do not "improve" it creatively.**

Deep detail in `references/`, real cases in `examples/`, verify against `references/checklist.md` before delivery.
Note: the reference and example files are written in Chinese; the rules themselves are language-independent.

---

## 1. Six hard rules

### Grid
12-column modular grid. Every edge sits on a grid line. Asymmetric composition, whitespace ≥ 35%. No centered symmetry.

### Type
Neo-grotesque only (Helvetica / Neue Haas Grotesk / Inter). Regular and Bold only.

### Alignment
Flush left everywhere, ragged right. Never centered, never right-aligned, never justified.

### Color
Three colors only: black `#000000`, off-white `#F2EFE8`, accent red `#DA291C`. Flat fill only.
No shadow, gradient, texture, noise, emboss, glow, glassmorphism. Red area ≤ 15%.

### Elements
Images only black-and-white photography or simple geometry. No decorative illustration, cartoon, 3D, icons, patterns, stickers. Dividers are 0.5–1pt hairline rules.

### Accents
Only two-digit indices `01` `02`, small year `1957`, place `ZÜRICH`, page numbers. No other symbols, no emoji.

---

## 2. Two-step type scale (the only permitted hierarchy)

```
MAX   Bold     headlines, key figures   spanning 6–8 columns
MIN   Regular  body, labels, meta       spanning 2–4 columns
```

**Two steps only.** No Medium, no subheads, no intermediate sizes. Any four-level scale is a fail.

---

## 3. Layout recipes

| Format | Top to bottom |
| :--- | :--- |
| Vertical poster 3:4 | `01` + year/place → oversized headline → tiny body → red block or photo anchor → hairline + footer |
| Horizontal cover 16:9 | `01` + category → oversized headline (left or right) → tiny body on the other side → horizontal hairline → footer |
| Data page | index + title → three data blocks (huge figure + tiny label + red bar) → source line |

---

## 4. Image prompt (minimal viable)

```
Swiss Style, [scene], 12-column modular grid, all elements aligned to grid lines
Type: neo-grotesque only, Regular and Bold; oversized headline + tiny body copy
Layout: flush left, ragged right, asymmetric, generous whitespace
Color: black, off-white #F2EFE8, accent red #DA291C only, flat fill
Elements: hairline rules, index 01, small year and place, [b/w photo / red rectangle]
Exclude: shadow, gradient, texture, decorative illustration, 3D, icons, emoji
```

---

## 5. Pre-delivery check

Four most common failures:

1. Headline centered → breaks the asymmetric grammar
2. A third or fourth color appears → three is the ceiling
3. Medium or Light weight appears → Regular and Bold only
4. A gradient or drop shadow was added → violates flat fill

Full checklist in `references/checklist.md`.

---

## 6. Common mistakes

| Mistake | Why it fails |
| :--- | :--- |
| Centered headline | Destroys flush-left asymmetric grammar |
| Medium / Light weights | Only Regular and Bold allowed |
| Gradient background or shadow | Violates flat fill |
| Illustration, icons, stickers | Decoration is banned |
| Four type sizes | Only two-step contrast allowed |
| Justified text | Must stay ragged right |
| A third or fourth color | Three-color ceiling |
| Rounded cards, pill buttons | Contemporary UI language, not Swiss |
| Filling the page, no whitespace | Whitespace is the subject, not leftover space |

---

## 7. Cases

| Case | Format | File |
| :--- | :--- | :--- |
| SWISS STYLE | Vertical poster 3:4 | `examples/01-poster.md` |
| GRID SYSTEM | Horizontal cover 16:9 | `examples/02-cover.md` |
| GRID AUDIT | Data page 3:4 | `examples/03-infographic.md` |
| FORM FOLLOWS | B/W photo mix 16:9 | `examples/04-photo.md` |

Each case records the brief, the full prompt, the output, and a review of where it drifted.

---

## 8. Adaptation

- **Print**: lay out to the real paper size; margin 6–8% of the short edge, never substitute screen ratios.
- **Screen**: 3:4 vertical, 16:9 horizontal, 1:1 social square.
- **Dense content**: merge duplicates and regroup columns first. **Never shrink type or delete facts** to make room.
- **Multi-page**: index position, page number position and red position fixed every page to build rhythm.

---

## Version

Current 0.2.0. Chinese spec: `SKILL.md`. Changes: `CHANGELOG.md`.
