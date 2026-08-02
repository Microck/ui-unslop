# UI Slop Pattern Catalog

Use this catalog during the audit. The target is not decoration itself. The target is decoration chosen by formula instead of product intent.

## Contents

1. Decorative pill badges and eyebrow tags
2. Gradient headline text
3. Formulaic heroes and scroll cues
4. Cookie-cutter sections and uniform card grids
5. Generic AI copy
6. Excess animation
7. Nested cards and double bezels
8. Homogeneous color goo
9. Generic decorative assets
10. Trend effects without brand ownership
11. Unjustified interface conventions

## 1. Decorative pill badges and eyebrow tags

Typical tell:

```html
<span class="rounded-full px-3 py-1 text-[10px] uppercase tracking-[0.2em] bg-pale-green/20 text-pale-green">
  Live on Solana
</span>
```

This pattern combines a tiny rounded pill, uppercase text, wide tracking, and a pastel fill above a heading.

Keep it when the shape communicates status, a category, or dense dashboard metadata. Remove or revise it when it decorates a hero or every section, especially labels such as "Live on [chain]," "Built with [X]," or "Est. [year]."

Better choices:

- Drop it and let the heading stand alone.
- Put useful metadata in navigation, a footer, or a plain meta line.
- Use a simple inline prefix such as `Solana /` or `2024 -`.
- Flatten a necessary label with an underline:

```html
<span class="text-xs font-medium text-ink-secondary border-b border-ink/20 pb-0.5">
  Solana
</span>
```

## 2. Gradient headline text

Typical tell:

```html
<h1 class="bg-gradient-to-r from-emerald via-violet to-amber bg-clip-text text-transparent">
  Build what's next
</h1>
```

Keep a gradient when it belongs to the brand or gives one accent word a restrained color shift. Revise it when a headline uses three or more unrelated colors, each section has a different gradient, or the colors do not belong to the brand palette.

Better choices:

- Use a solid color and change one word's weight or color.
- Shift subtly between nearby hues.
- Pair serif and sans-serif type for contrast.
- Let size and weight create hierarchy.

## 3. Formulaic heroes and scroll cues

Typical sequence:

1. Decorative pill
2. Giant gradient headline
3. Muted subtitle around 18px
4. Solid primary CTA beside an outlined secondary CTA
5. Scroll indicator

Use a structure that fits the content instead:

- Asymmetric: left-aligned headline with a useful visual beside it.
- Minimal: product name, one line, and deliberate whitespace.
- Editorial: strong type and body copy, with an inline text link instead of ornamental buttons.
- Split: text on one side and one strong visual on the other.

Remove "Scroll to explore," down arrows, and other scroll cues unless users need explicit help to discover unusual scrolling behavior.

## 4. Cookie-cutter sections and uniform card grids

Typical tell: every section repeats `label -> heading -> subtitle -> card grid` with the same width, spacing, and rhythm.

Better choices:

- Match spacing to the content instead of repeating one padding value.
- Alternate constrained text with full-width material when the content calls for it.
- Open with a quote, statistic, image, or direct content rather than a label.
- Merge sections that do not need separate framing.
- Use a rule or divider when it clarifies structure.

Variation must clarify content. Random inconsistency is not personality.

Do not force unrelated ideas into identical cards. Choose a list, comparison, prose block, diagram, table, or unboxed layout when that structure fits the content better.

## 5. Generic AI copy

Remove these filler words and formulas from markup unless they are quoted or have a precise domain meaning:

- Elevate
- Seamless
- Unleash
- Next-Gen
- Game-changer
- Delve
- Revolutionary
- Cutting-edge
- Innovative
- Empower
- Transform
- Supercharge
- The future of [X]
- [X] redefined
- Welcome to [X] as hero text

Replace aspiration with a concrete action or fact. For example, use "Swap on Jupiter" instead of "Experience the future of trading." When no useful detail exists, use less copy.

## 6. Excess animation

Typical tells:

- every element fades upward on scroll
- every hover scales or translates
- every list staggers its reveal
- several background blobs animate at once
- CSS defines five or more unrelated animations for one page
- cards lift and change shadow by default

Keep motion when it explains a state change, gives useful interaction feedback, or supports one intentional entrance or ambient moment. Most content should appear immediately and remain stable. Honor reduced-motion preferences.

One hero entrance, subtle feedback on interactive controls, and at most one ambient element are reasonable bounds. As a cleanup heuristic, cut roughly 80 percent of decorative animation before deciding whether any should return.

If removing motion makes the page dull, improve the layout rather than restoring ambient effects.

## 7. Nested cards and double bezels

Typical tell: most cards use an outer shell plus a nested inner core, or several containers nest without clarifying ownership or interaction.

Reserve a double bezel for one or two hero feature cards or product showcases. Flatten cards-inside-cards into spacing, headings, dividers, or one meaningful container. Use a simple border and background for ordinary grids, FAQs, statistics, and footer links.

## 8. Homogeneous color goo

Typical tell: many similar tinted chips, panels, and accents compete at the same visual weight without establishing hierarchy.

Start from a neutral base, one intentional accent, and semantic state colors. Use color to communicate brand, state, or importance rather than to fill every available surface.

## 9. Generic decorative assets

- **Icons in colored rounded boxes:** Keep the box only when it encodes a real category or state. Prefer a domain-specific icon, a coherent illustration system, or no icon when the asset adds no information.
- **Emoji as visual assets:** Reserve emoji for user content or a voice that intentionally uses them. Use consistent icons, illustrations, or plain text for product features.
- **Fake browser chrome:** Remove ornamental red, yellow, and green dots. Show an accurate product frame when browser context matters, or crop to the product itself.
- **Empty gradient visual placeholders:** Replace decorative gradient rectangles with a real product view, useful diagram, relevant image, or deliberate whitespace.
- **Particle and connect-the-dots backgrounds:** Keep them only when they belong to the brand or explain real data. Otherwise, use composition and content to create interest.

## 10. Trend effects without brand ownership

- **Trendy serif heroes:** Use a display serif only when the subject and type system support it. Do not add one solely to make a generic page feel premium.
- **Glassmorphism everywhere:** Use blur and transparency only when they communicate depth or material relationship. Prefer legible opaque surfaces for ordinary content.
- **Gradient and glow buttons:** Establish action hierarchy with label, placement, contrast, and a solid treatment. Reserve glow for a brand-owned effect and never let it imitate focus state.
- **Rounded left-border callouts:** Use a semantic alert or callout style when the message has real status. Avoid the rounded card plus colored stripe as default decoration.

## 11. Unjustified interface conventions

- **Decorative numbered sections:** Use `01`, `02`, and `03` only for a real sequence, ranking, or stable reference.
- **Four-column stat strips:** Show verified, relevant evidence instead of default SaaS counters. Remove weak or invented numbers.
- **Floating chat bubbles:** Add one only when a real support channel exists, the control works, and persistent placement serves the workflow.

## Final test

Ask whether each visible choice follows from the product, content, or brand. If its only rationale is that generated interfaces commonly use it, remove or replace it.
