---
brand_id: hw-red
kind: brand
summary: hwppt house identity — one deep-red accent on a white field with gray structure, for Chinese planning, platform, and engineering-process decks
primary_color: "#B5121B"
---

# hw-red Brand Specification

> Identity-only preset. No SVG page roster — pages are composed freely under these constraints. This is the default identity of the `/hwppt` command; it is a house palette, not any company's official brand.

## I. Brand Overview

| Property | Value |
|---|---|
| Brand Name | hw-red（红白图示） |
| Use Cases | R&D process and platform planning, tool / platform rollout, technical solution walkthroughs, team planning shares, promotion and job-review (任职汇报) decks, internal training |
| Tone | Calm, engineering-literate, evidence-led; red is a pointer, never decoration |
| Sources | Distilled from the OMP SDD planning decks iterated with the user in 2026-10 (versions 19–25). Every value is a house choice confirmed by the user (provenance `user`), not taken from any external brand manual |

## II. Color Scheme

| Role | HEX | Provenance | Notes |
|---|---|---|---|
| primary | `#B5121B` | user | The single accent. Current stage, the one key conclusion on a page, numbered step circles, the one bar that spans the whole flow |
| accent | `#333333` | user | Body text and dark structure |
| bg | `#FFFFFF` | user | White page field; a pale gray geometric wash may sit in the lower-right corner as the only background ornament |
| surface | `#F2F2F2` | user | Neutral modules, platform / base layers, gray pills |
| border | `#D1D1D1` | user | Hairlines, card strokes, inactive navigation |
| muted-text | `#737373` | user | Subtitles, labels, captions, footers |
| tint | `#FBEFF0` | user | "Look here" fill — always paired with a primary-red stroke |
| tint-strong | `#F3C9CC` | user | Second chart series, middle pyramid tier, secondary bars |
| charcoal | `#4D4D4D` | user | Framework-type means tags, the team / foundation band |

Color discipline (the part that matters most):

- **One solid red per page.** A page has exactly one solid-red element or one homogeneous set (e.g. the active chevron, or a row of step numbers). Every other emphasis is "red stroke + pale tint".
- Red marks *where to look*, not danger. Do not use it for warnings unless the page is literally about risk; never put body text on a large red fill.
- No other hues. Do not introduce blue / green / orange series; use red → tint-strong → tint → gray for ordered series. The only exception is a UI mock (window buttons) explicitly labelled 示意.
- No gradients, glows, or drop shadows. Flat planes and hairlines only.

## III. Typography

| Role | Family | Weight |
|---|---|---|
| title | `"Microsoft YaHei", "PingFang SC", Arial, sans-serif` | 700 |
| body | `"Microsoft YaHei", "PingFang SC", Arial, sans-serif` | 400 |

> Microsoft YaHei is the delivery font because the audience presents on Windows PowerPoint; never ship a macOS-only face (Heiti SC, PingFang) as the first family. Title ≈ 31–32 pt red bold, one line, no trailing period; subtitle ≈ 18 pt gray, one line. Inside diagrams keep body ≥ 14 px and captions ≥ 13 px on a 1280-wide canvas; only one-page overview / dashboard-mock pages may go denser.

## IV. Logo

- File: `none`
- Usage: never

No logo is bundled. Put the team or project name as editable footer text in the deck's own typography.

## V. Voice & Tone

- Formality: formal
- Person: 我们 / 团队 (Chinese); we (English)
- Emoji: forbidden
- Abbreviations: spell-out-first-use

> Write in the user's purpose voice: a planning share explains how and why, a report to leadership leads with the conclusion and ends with decisions. Unify every term deck-wide; first use spells the full name, then the short name; collect English abbreviations in a closing glossary.

## VI. Icon Style

- Preference: stroke

> One stroke family (for example `tabler-outline`) in primary red or muted gray, sitting in a pale-tint circle when it labels a card. Icons clarify a role, state, or object (document, person, database, gear, shield, clock); never decorate.
