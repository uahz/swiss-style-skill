# swiss-style-skill

[中文](README.md) · **English**

> A Swiss Style (International Typographic Style) design skill package for AI.
> Turns the visual grammar of 1950s International Typographic Style into a reusable Skill and a set of ready-to-apply layout specs.

<p>
  <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-DA291C?style=flat-square&labelColor=000000">
  <img alt="Typography" src="https://img.shields.io/badge/Font-Helvetica%20%2F%20Inter-000000?style=flat-square&labelColor=000000">
  <img alt="Grid" src="https://img.shields.io/badge/Grid-12%20Columns-000000?style=flat-square&labelColor=000000">
  <img alt="Palette" src="https://img.shields.io/badge/Palette-3%20Colors-000000?style=flat-square&labelColor=000000">
</p>

## Preview

<table>
  <tr>
    <td width="45%"><img src="assets/preview-poster.png" alt="Vertical poster sample: SWISS STYLE"></td>
    <td width="55%"><img src="assets/preview-cover.png" alt="Horizontal cover sample: GRID SYSTEM"></td>
  </tr>
  <tr>
    <td><sub>Vertical poster · 3:4 · index + year/place + oversized headline + tiny body + red geometric anchor</sub></td>
    <td><sub>Horizontal cover · 16:9 · asymmetric columns + hairline rule + single red accent</sub></td>
  </tr>
</table>

Both samples are AI-generated output, used to prove the rules are executable: 12-column grid, two-weight contrast, flush left, flat three-color palette, zero decoration.

## Features

- **12-column modular grid**: every edge snaps to a grid line; asymmetric composition; whitespace ≥ 35%
- **Neo-grotesque type only**: Helvetica / Neue Haas Grotesk / Inter, Regular and Bold only
- **Extreme scale contrast**: oversized headline + tiny body, ratio ≥ 4:1, no intermediate sizes
- **Flush left everywhere**: ragged right, never centered, never justified
- **Three-color system**: black `#000000` / off-white `#F2EFE8` / accent red `#DA291C`, red area ≤ 15%
- **Flat fill only**: no shadow, gradient, texture, decorative illustration, or 3D
- **Restrained accents**: hairline rules, `01` `02` indices, small year and place labels

## Files

| File | Purpose |
| :--- | :--- |
| `SKILL.md` | Full skill definition: hard rules, grid spec, layout hierarchy, checklists, common mistakes |
| `templates/image-prompt.md` | Image prompt templates (generic / vertical poster / horizontal cover / infographic / photo mix / negative prompt) |
| `templates/poster-layout.md` | Vertical poster spec: grid coordinates, 5-layer structure, 3 compositions |
| `templates/cover-layout.md` | Horizontal cover and info page spec: hierarchy, composition, multi-page continuity |
| `assets/` | Style samples (vertical poster / horizontal cover) |
| `LICENSE` | MIT |

Note: `SKILL.md` and the layout specs are written in Chinese. The rules themselves are language-independent — the prompt templates can be used as-is, and you can translate the spec text if you need an English-only variant.

## Usage

### 1. Use it as a prompt

1. Open `templates/image-prompt.md`
2. Copy the template for your case
3. Replace `[scene]` with your subject
4. Paste into any image generation tool

### 2. Install it as a Skill

`SKILL.md` ships with YAML frontmatter (`name` / `description`) and follows the common skill convention. Drop it into the skills directory of any client that supports custom skills:

```
<skill_root>/swiss-international-style/SKILL.md
```

Works with Cherry Studio, Coze, and most agent frameworks.

### 3. Use it as an acceptance spec

Hand the checklist in `SKILL.md` to a designer or an outsourcer as the review standard. It removes most of the back-and-forth on "make it cleaner / bolder / more premium".

## Quick example

```
Swiss Style poster, 12-column modular grid, all elements aligned to grid lines
Type: neo-grotesque only (Helvetica / Neue Haas Grotesk / Inter), Regular and Bold only
Layout: flush left, ragged right, asymmetric, generous whitespace, no centering
Scale: oversized headline + tiny body copy, strong contrast, no intermediate sizes
Color: black, off-white #F2EFE8, accent red #DA291C only, flat fill
Elements: hairline rules, index 01, year 1924-2024, one red geometric rectangle
Exclude: shadow, gradient, texture, decorative illustration, 3D, icons
```

## Common mistakes

| Mistake | Why it breaks the style |
| :--- | :--- |
| Centered headline | Destroys the flush-left asymmetric grammar |
| Medium / Light weights | Only Regular and Bold are allowed |
| Gradient background or drop shadow | Violates flat-fill principle |
| Illustration, icons, stickers | Decoration is banned |
| Four type sizes (XL / L / M / S) | Only two-step contrast is allowed |
| Justified text | Must stay ragged right |
| A third or fourth color | Three colors is the ceiling |

## License

MIT. Free for commercial use, modification, and redistribution.

## Credits

Visual rules derive from Josef Müller-Brockmann's *Grid Systems in Graphic Design* and the Zurich / Basel school practice of the 1950s–60s.
