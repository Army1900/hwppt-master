---
style_id: hw-plan-share
kind: style
summary: Question-spine planning method — conclusion titles, one diagram per page, overview-first and full-view bookend, honest placeholders, every rule tied to its enforcing means.
keywords: [planning, diagram-first, conclusion-title, rollout, engineering-process]
---

# hw-plan-share — Style Specification

> Method and design defaults only. No project communication contract, brand identity, page structure, or SVG prototypes. This is the default method of the `/hwppt` command.

## I. Style Overview

| Property | Value |
|---|---|
| Style Name | hw-plan-share（规划分享 · 图示优先） |
| Best Fit | R&D process / platform planning, tool or platform rollout, technical solution walkthroughs, team planning shares to leadership and team at once, promotion / job-review decks |
| Reusable Intent | Make a dense engineering plan readable from its titles alone, carry every page by one diagram, keep claims honest when data is missing, and make every rule show how it is enforced |
| Sources | Distilled from the OMP SDD planning decks iterated with the user in 2026-10 (versions 19–25): logic-flow review, text-to-diagram rewrite, plan-voice rewrite, full-view house page, dedupe and terminology passes |

## II. Communication Method

- **Preferred Mode**: custom
- **Mode References**: pyramid, instructional
- **Mode Behavior**: A question spine carries the deck: 为什么做 → 怎么做 → 怎么保障 → 用得怎么样 → 怎么推广 (rename to fit the topic; 3–6 parts). pyramid owns the page level — every page title states its answer; instructional owns the part level — each part decomposes one question into parallel, teachable pages. Open with a one-page overview (the spine plus 3–4 key practices); close with a full-view "house" page that rebuilds the whole plan on one page, then a glossary.
- **Argument Flow**: Establish the premise before the procedure (e.g. "one requirement = one repository = several boundary units" precedes the five-stage flow, otherwise later pages use undefined boundaries). In the "how is it going" part, lead with one real case, then define the measurement basis, then show the dashboard / platform that carries it, then problems and the improvement loop — define a metric before showing it. Never end on roles or risks; end on the full view.
- **Page Message Discipline**: Every title is a complete claim of at most about 26 Chinese characters, no trailing period (e.g. 「阶段④：人工审批后才能合入，AI 不直接进主干」, not 「阶段④ 代码检查」). One subtitle line adds the why / how. Reading the titles alone must tell the whole story. Do not add a separate takeaway line that repeats the title; details, definitions, and sources go to speaker notes.
- **Claim Discipline**: Never invent numbers. Where real data is missing, author editable placeholder text boxes (「__ 天」「待填」) inside dashed frames, or label the figure 示意数据 / 示例 / 建议值, and say so in the notes. Keep user-stated facts separate from inferred risks or gaps; inferred items are marked in the notes as 推断 / 待试点确认. When the user corrects a fact (ID format, version format, when data is uploaded, cross-repo rules), propagate it to every page, including mock data formats.
- **Voice by purpose**: A planning share or team briefing explains how and why and contains no decision requests or 「需要的支持」 asks; rename such a page to 「团队怎么一起做」. A report for a decision opens with a one-page conclusion and closes with a decision table (item / proposal / owner / date, with owner and date as placeholders). A job-review deck may lead with the full-view page.
- **One concept, one home**: Fully develop each concept on exactly one page and point to it elsewhere in one line (「放行条件见各阶段页」). Typical repeats to remove: the same team roles on 3–4 pages, the same gate conditions on overview + stage + guarantee + exception pages, the same boundary rule on two pages.
- **Terminology**: One term per meaning across titles, diagrams, notes, and glossary. Example split: 放行条件 = what must hold, 人工确认 = who confirms; do not mix in 检查点 / 把关 / 看护 for the same idea. Stage names are identical in navigation, overview, stage pages, dashboards, and case pages. First use spells the full term (titles count).
- **Rules carry their means**: When a page states a constraint, show the rule, the means that enforces it, and the stage where it applies. Tag means in five kinds — 平台 (design platform), 框架 (architecture-test framework), 指标 (coverage), 测试 (integration test), 人工 (review) — so "AI 提速，规则兜底" is visibly backed.
- **Discuss before restructuring**: When the user says 先讨论, return a ranked diagnosis (structure > duplication > terminology > small fixes) and wait; do not edit.

## III. Page Role Vocabulary

| Role | Communication Job | Evidence Obligation | Composition Tendency |
|---|---|---|---|
| One-page overview | Show the question spine and the few practices that answer it | Each spine node states its answer in two short lines; no new facts | Numbered circles across the top connected by arrows, a row of 3–4 practice cards below |
| Section divider | Say which question this part answers | One-line answer; part number | Oversized part number, five-part navigation with the current part in red |
| Premise / unit of work | Define the unit everything else operates on | User-stated rules (ownership, boundaries, platform constraints) | Two panes: decomposition + workspace on the left, unit types and granularity rules on the right, collaboration flow at the bottom |
| Layered positioning | Explain why a custom layer sits on a general platform | Which needs come from the business, what the platform already provides | Three horizontal layers (business → custom → platform), the custom layer tinted, upward "reuse" arrows |
| Full flow | Show all stages with artifacts and human confirmation points | Artifact per stage, who confirms | Swimlanes: stage chevrons / artifact document icons / person-icon gates |
| Stage page | One stage as input → steps → output, plus its gate | Inputs, outputs, gate condition, tools | Stage navigation on top, inputs left, 3–5 numbered steps centre (dashed loop when iterative), outputs right, a tinted gate bar, tool pills |
| Guarantee matrix | Show which guarantee covers which stages and by what means | Means per guarantee, stage coverage | Rows = guarantees with means tags; bars spanning stage columns; only the cross-cutting row solid red |
| Layered constraint | Per architecture layer: responsibility, constraint, enforcing means | Rules and tools actually in use (mark "已在用，需加强" honestly) | Layer stack on the left with dependency arrows, constraint text centre, means tags right |
| Tiered standard | Graded thresholds (key / new / legacy) | Thresholds marked 建议值 unless confirmed | Three-tier pyramid with big metric callouts and rule pills |
| Exception backflow | What happens when a gate fails and when to escalate | Example failures labelled 示例 | Stages with ✓ diamonds and dashed return loops; escalation cards; how-found pills |
| Real case | Replay one finished task stage by stage | Real data only; otherwise editable placeholders | KPI tiles on the left, stage × (time / artifacts / problems) on the right, a totals bar |
| Measurement basis | What is measured and what is explicitly not | Sources, formula, exclusions | Source pills → association hub → 3 metric cards → formula bar → "不看" pills |
| Platform / dashboard | Introduce a system by showing it | Mock data marked 示意数据 | A window-framed UI mock on ~¾ of the page, numbered badges matching 3–4 design notes on the right |
| Improvement loop | Problem → action → asset update → re-check | Examples labelled 示例 | Four-node cycle with result pills in the centre, example cards and cadence pills on the right |
| Rollout roadmap | Phases, workstreams, milestones, decision fork | Weeks are 建议节奏 | Gantt rows across phase bands, milestone diamonds, a three-way fork (扩大 / 继续 / 调整), milestone cards below |
| Team support | Who does what to keep the platform running | Effort as placeholders | Usage → role cards (with effort placeholders) → platform; risk → mitigation pairs |
| Full-view house | Rebuild the whole plan on one page | Only content already shown | Roof = vision, rows = goals / stages / guarantees / measurement / platform base, foundation band = team, side columns = scenarios & risks / rollout rhythm |
| Glossary | Plain-language terms | Team's own usage | 3-column term cards |

## IV. Evidence & Data Expression

- **Argument Trace**: Each page title must be supported by what is drawn on that page; each part must answer its spine question. Missing evidence stays visible as a placeholder or an explicit "暂不给出结论".
- **Charts**: Prefer structure diagrams over charts; when a chart is needed, ordered series use red → tint-strong → tint → gray, labels are direct, and mock values are labelled 示意.
- **Tables**: Convert tables to diagrams (flow, matrix bars, swimlanes, layer stacks, roadmap, cycle, pyramid) unless the user must edit the cells; a fill-in table becomes a page of editable placeholder text boxes.
- **Sources**: Put provenance, definitions, and "来自团队描述 / 推断" notes in speaker notes, not on the slide.
- **Native Editability**: Titles, subtitles, footers, page numbers, and every placeholder are native editable text. Diagrams use native shapes so the user can adjust them in PowerPoint.

## V. Visual System Defaults

- **Preferred Visual Style**: custom
- **Visual Style References**: swiss-minimal, soft-rounded
- **Visual Style Behavior**: swiss-minimal owns the flat field, hairlines, grid alignment, and the absence of ornament; soft-rounded owns only the small corner radius (6–12 px) on cards, pills, and chevrons — no elevation, no shadows. The recurring motif set: chevron stage navigation, red numbered step circles, diamond + check for gates and milestones, dashed return loops for backflow, document icons (gray for inputs, red for outputs), pale-tint circles behind stroke icons, rounded pills for tools and means tags. A pale gray geometric wash in the lower-right corner of every page is the only background ornament.
- **Composition**: Title and one-line subtitle top-left; one diagram fills the body; footer left (deck name + part), page number right. Diagrams read left-to-right or top-to-bottom with one scan path. Navigation chevrons sit at the top of stage-type pages so the viewer always knows where they are.
- **Density**: Ordinary pages stay around 150 visible characters inside the diagram; trim words before shrinking type, split the page before going below 13 px. Overview, full-view house, and dashboard mock pages may be denser and are meant to be read up close.
- **Decoration**: No title underlines, edge stripes, single-side card borders, gradients, emoji, or bitmap icons. Separation comes from whitespace, hairlines, and tinted fills.
- **Color Behavior**: White field; gray builds structure; one solid red element per page points to the focus; "red stroke + pale tint" marks secondary focus; gray pills and gray layers are neutral. A confirmed Brand identity replaces the fallback palette below; the one-solid-red rule still applies to its primary color.
- **Typography Character**: One sans-serif family; titles bold red, subtitles gray, diagram labels dark gray with weight for hierarchy. No display faces, no text effects.

### Fallback Color Scheme

| Role | HEX | Purpose |
|---|---|---|
| background | #FFFFFF | Page field |
| primary | #B5121B | The one solid focus element; title color; step numbers |
| body_text | #333333 | Body text and labels |
| secondary_text | #737373 | Subtitles, captions, footers |
| surface | #F2F2F2 | Neutral modules, platform layers, gray pills |
| divider | #D1D1D1 | Hairlines, card strokes, inactive navigation |
| tint | #FBEFF0 | Secondary focus fill, always with a red stroke |
| tint_strong | #F3C9CC | Second series, middle tiers |
| charcoal | #4D4D4D | Framework means tags, foundation band |

### Fallback Typography

| Role | Primary | Fallback Tail | Character |
|---|---|---|---|
| title | Microsoft YaHei | PingFang SC, Arial, sans-serif | Bold, one line, the claim carries the force |
| body | Microsoft YaHei | PingFang SC, Arial, sans-serif | Same family; compact labels inside diagrams |

A supplied Brand or Deck identity replaces this fallback palette and typography wholesale; the method and layout rules are unaffected.

## VI. Image & Icon Direction

- **Preferred Image Rendering**: flat
- **Image Usage**: Default to no photographs or generated illustrations; diagrams carry the content. Use an image only for a real screenshot or evidence the user supplies.
- **Image Treatment**: Real screenshots sit in a hairline frame with a caption; UI that does not exist yet is drawn as a native mock labelled 示意数据, never generated as an image.
- **Icon Treatment**: One stroke family, red or gray, in pale-tint circles when labelling cards; icons name roles and objects (document, person, database, gear, shield, clock, chat) and never decorate.

## VII. Review Focus
<!-- visual-review-trigger: explicit-user-only -->
> Apply this section only after the user explicitly activates visual review. It never triggers that stage.

- Reading only the titles tells the whole story; no topic-only titles remain.
- The deck opens with an overview and closes with a full-view / conclusion page before the glossary.
- Each page has one diagram and at most one solid-red element; no text below 13 px on ordinary pages; nothing overflows or touches its frame.
- No concept is fully developed on more than one page; stage names and key terms are identical everywhere.
- Every number is real, a placeholder, or labelled 示意 / 建议值; viewer-facing hints such as 「灰字为待填」 live in notes, not on slides.
- Every stated rule shows its means and stage; the voice matches the purpose (no decision asks in a planning share).
- Page numbers in the outline and in notes match the current order.
