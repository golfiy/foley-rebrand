# Foley Deck — AI generation config

A loadable spec for Gamma, Tome, Beautiful.ai, Pitch AI, or any LLM‑driven deck tool. Two parts:

1. **Theme + layouts schema** (YAML) — paste this as the system style or attach as a reference doc.
2. **Generation prompt** (markdown) — paste into the "Generate a presentation" field.

Both are below. Do not edit the schema unless brand rules change. Edit only the **CONTENT BRIEF** at the bottom of the prompt to fit a specific use case.

---

## 1. Theme + layouts schema

```yaml
# foley-deck-config.yaml — v1
# Feed this whole block to the deck tool as the brand spec.

theme:
  name: Foley
  version: 1.0
  surface_default: paper       # paper | mist | navy
  aspect: 16:9
  baseline_size: 1280x720

brand:
  name: Foley                   # NEVER "Foley Services" or "Foley Carrier Services"
  domain: foley.io
  email: marketing@foley.io
  tagline: "Smarter Data. Lower Risk. Safer Fleets."
  promise: "Get your fleet to clear — and keep it there."
  positioning: "All-in-one compliance, safety, and screening platform for commercial fleets — from 5 drivers to 500."
  audience:
    - Safety / HR directors
    - COO, CFO
    - Industries: transportation, retail, construction, agriculture, healthcare, manufacturing
  trust_proof_points:           # use sparingly, never list all in one slide
    - "50,000+ companies trust Foley"
    - "#1 DOT Compliance Provider"
    - "4.3★ Trustpilot · 1,124 reviews"
    - "30 years of compliance expertise"
  product_names:                # use exactly, do not abbreviate
    - CSA Monitoring
    - MVR Monitor
    - Audit Risk Monitor
    - Hiring & Onboarding
    - Background Checks
    - Foley Navigator AI
    - Drug & Alcohol Testing
    - DOT Physicals
    - FMCSA Clearinghouse
  flywheel_forces:              # the 5 canonical Foley Flywheel forces
    - Great People Winning Together
    - Dominant Vertical Solutions
    - Exceptional Marketing & Sales Execution
    - 6-Star Customer & Candidate Experience
    - Annual Recurring Revenue Growth
  flywheel_center: "Screening and compliance for drivers and safety-sensitive employees"

logo:
  primary_url:    "https://golfiy.github.io/foley-rebrand/assets/image30.png"  # full color wordmark on light
  symbol_url:     "https://golfiy.github.io/foley-rebrand/assets/image29.png"  # rings only
  symbol_white:   "use CSS filter: brightness(0) invert(1) on the wordmark for dark surfaces"
  rules:
    - "DO NOT redraw, recolor, restroke, or replace the supplied logo."
    - "Min size: 24 px tall on a 1280x720 slide."
    - "Clearspace: at least the height of the lowercase 'o' on every side."
  placement_by_layout:
    cover:           "wordmark · top-left"
    cover_contact:   "wordmark · top-left"
    section:         "wordmark · top-left, slide counter top-right"
    content:         "wordmark · top-left, slide counter top-right"
    closing:         "wordmark · top-left"

palette:
  surfaces:
    primary_dark:    { hex: "#0B1F3A", name: "Foley Navy",       use: "covers, section dividers, executive panels" }
    primary_dark_2:  { hex: "#061429", name: "Foley Navy Deep",  use: "layered dark backgrounds" }
    soft:            { hex: "#F2F6FB", name: "Mist",             use: "alternate content sections" }
    primary_light:   { hex: "#FFFFFF", name: "Paper",            use: "default content slides" }
  accent:
    brand:           { hex: "#2D8FE8", name: "Foley Blue",       use: "ONLY brand accent — KPI highlights, links, primary buttons" }
    deep:            { hex: "#1B6FBF", name: "Foley Blue Deep",  use: "hover state, secondary accent" }
    sky:             { hex: "#5DBAEF", name: "Foley Sky",        use: "lighter accent, echoes the logo's inner cyan, illustration accents" }
    soft_tint:       { hex: "#E5EFFB", name: "Foley Tint",       use: "tag bg, hover surfaces" }
  semantic:                      # NEVER use as brand colors — semantic states only
    success:         { hex: "#2EA86A", use: "ONLY for cleared/passed/OK status indicators" }
    risk:            { hex: "#E5484D", use: "ONLY for errors, violations, comparison X marks" }
    caution:         { hex: "#F4B740", use: "ONLY for warnings, attention needed" }
  text:
    ink:             { hex: "#0B1828", use: "primary body on light surfaces" }
    ink_soft:        { hex: "#3A4A5E", use: "lede, captions, secondary text on light" }
    muted:           { hex: "#6B7B8E", use: "meta, timestamps, footer text, axis labels" }
    line:            { hex: "#E1E7EF", use: "1px borders, dividers, hairline rules" }
  forbidden:
    - "yellow / orange gradients (the brand FAQ says: moving away from yellow/orange tones)"
    - "red as a brand color"
    - "green as a brand color (green is reserved for cleared status only)"
    - "multicolor pie charts"
    - "drop shadows on text or buttons"
    - "gradients with more than 2 stops"

typography:
  display:
    family: "Inter Tight"
    weight: 700
    case: "sentence case ONLY"   # NEVER ALL CAPS for headlines
    tracking: "-2.5%"
    line_height: 0.98
    sizes_px: { hero: 96, h1: 64, h2: 44, h3: 28 }
  body:
    family: "Inter"
    weight: 400
    line_height: 1.6
    max_width: "70ch"
    sizes_px: { lede: 20, body: 16, caption: 13 }
  mono:
    family: "JetBrains Mono"
    weight: 500
    use: "KPI values, dates, percentages, axis labels, footer counters, eyebrow labels"
    sizes_px: { kpi: 14, meta: 12, caps_label: 11 }
  rules:
    - "NEVER use ALL CAPS for headlines. Eyebrow labels (≤12 px mono) only."
    - "NEVER use Title Case Headings. Sentence case only."
    - "NEVER use Arial. Inter Tight + Inter + JetBrains Mono only."
    - "Use tabular numerals for numbers (font-feature-settings: tnum)."

spacing:
  unit: 8                        # px
  slide_margin_pct: 5            # of slide width
  vertical_rhythm: 1.5

imagery:
  photography:
    style: "documentary editorial — real fleets, drivers, depots, dispatch rooms, warehouses"
    avoid: "stock handshakes, staged offices, cartoon clipart, multicolor flat illustrations"
    treatment: "navy/blue tonal grade; never warm yellow/orange filters"
    overlay_rule: "linear-gradient(rgba(11,31,58,.4) 0%, rgba(11,31,58,.55) 50%, rgba(11,31,58,.92) 100%) over hero photos for text legibility"
  icons:
    library: "Lucide / Phosphor / Heroicons outline"
    stroke: "1.5 px"
    color: "Foley Blue Deep on light surfaces; white on dark"
    forbidden: "filled icons, multicolor icons, cartoon-style icons"
  decoration:
    allowed: "subtle dot grid (2 px dots, 24 px gap, 5–8% opacity) on Navy"
    forbidden: "abstract swooshes, blob shapes, beveled buttons, drop shadows"
  charts:
    style: "Swiss minimal — single accent color, thin axis lines, mono labels, generous whitespace"
    line_weight: "2–2.5 px"
    foley_series_color: "#2D8FE8"
    benchmark_color: "#6B7B8E (dashed)"
    fill_opacity: "10–18% for area fill under lines"

layouts:
  # 22 layouts — every slide must match one. Do not invent new ones.

  - id: 01_cover
    name: Cover
    surface: navy
    treatment: full-bleed photo with dark gradient overlay
    slots:
      - { name: logo,     position: top-left,                    asset: logo.primary }
      - { name: meta,     position: top-right,                   type: mono caption ("Investor briefing · Q2 2026") }
      - { name: eyebrow,  position: bottom-left-above-title,     type: small uppercase mono in Foley Blue }
      - { name: title,    position: bottom-left,                 type: H1 hero, max_width: 14ch, italicize_one_word: true }
      - { name: sub,      position: below-title,                 type: body lede, opacity: 0.78 }
      - { name: footer,   position: bottom-right,                type: mono "foley.io · date · classification" }

  - id: 02_cover_contact
    name: Cover with photo + contacts
    surface: split (paper left + photo right)
    slots:
      - { name: eyebrow, position: top-left-of-text-side, type: mono }
      - { name: title,   type: H1, max_width: 13ch, italicize_one_word: true }
      - { name: sub,     type: body lede }
      - { name: contacts, type: 3 mono rows with outline icons (mail / web / calendar) }
      - { name: photo,    side: right, treatment: subtle navy edge gradient }

  - id: 03_section_photo
    name: Section title — photo
    surface: navy with hero photo
    slots:
      - { name: numeral, position: top-right, type: huge Inter Tight 800, color: "rgba(45,143,232,.18)" }
      - { name: eyebrow, position: bottom-left-above-title, type: small uppercase mono in Foley Blue }
      - { name: title,   position: bottom-left, type: H2, max_width: 14ch }
      - { name: lede,    position: below-title, type: body, opacity: 0.7 }

  - id: 04_section_navy
    name: Section title — navy gradient
    surface: navy gradient (no photo)
    slots: same as 03_section_photo

  - id: 05_agenda
    name: Agenda
    surface: split (photo left + paper right)
    slots:
      - { name: photo,    side: left, treatment: navy gradient overlay }
      - { name: eyebrow,  side: right, type: mono }
      - { name: title,    type: H2 ("Agenda") }
      - { name: items,    type: numbered list, count: 5-6, numerals: JetBrains Mono ("01"..), divider: hairline rule between items }

  - id: 06_title_photo_cards
    name: Title + 3 photo cards
    surface: split (navy panel left + paper right)
    slots:
      - { name: panel_eyebrow, side: left, type: mono }
      - { name: panel_title,   side: left, type: H2 white }
      - { name: panel_body,    side: left, type: body, opacity: 0.72 }
      - { name: cards,         side: right, type: 3 horizontal cards each with: circle photo (56px), mono label, H3, body }

  - id: 07_title_3numbered
    name: Title panel + 3 numbered
    surface: split (navy panel left + paper right)
    slots:
      - { name: panel,  side: left,  type: navy panel with eyebrow + H2 + body }
      - { name: items,  side: right, type: 3 items each with mono numeral + subhead H3 + 2-line body }

  - id: 08_4numbered_panel
    name: 4 numbered + navy panel
    surface: mirrored — content left, navy panel right
    slots:
      - { name: items, side: left,  type: 4 items each with mono numeral + subhead + body }
      - { name: panel, side: right, type: navy panel with eyebrow + H2 + 2 short paragraphs }

  - id: 09_title_2cards
    name: Title bar + 2 cards
    surface: paper
    slots:
      - { name: titlebar, type: clean (no navy fill) — eyebrow + H2 + slide counter }
      - { name: cards,    count: 2, style: white card, 1px border, 2px Foley Blue accent on top, mono numeral + subhead + bullets }

  - id: 10_title_3cards
    name: Title bar + 3 cards
    surface: paper
    slots: same shape as 09 with count: 3

  - id: 11_title_4cards
    name: Title bar + 4 cards
    surface: paper
    slots: same shape as 09 with count: 4 (tighter)

  - id: 12_quadrants
    name: Four quadrants
    surface: paper
    slots:
      - { name: titlebar, type: clean }
      - { name: quads, count: 4, separator: hairline crosshair (#E1E7EF), each: mono numeral + subhead + body }

  - id: 13_social_proof
    name: Social proof
    surface: paper
    slots:
      - { name: titlebar, type: clean with eyebrow ("4.3★ Trustpilot · 1,124 reviews") }
      - { name: cards,    count: 4, style: white card with 1px border, contains: 5 stars (Foley Blue), pull quote H3-styled, photo avatar + name + role }

  - id: 14_photo_collage
    name: Title + photo collage
    surface: split (navy panel + bento photo grid)
    slots:
      - { name: panel,  side: left,  type: navy with eyebrow + H2 + body }
      - { name: bento,  side: right, type: 5-tile bento grid (one tile spans 2 cols) with documentary photos and tiny mono labels }

  - id: 15_flywheel
    name: Foley Flywheel
    surface: paper
    slots:
      - { name: titlebar, type: clean ("Foley Flywheel") }
      - { name: wheel,    type: 5-segment radial (Navy, Blue Deep, Blue, Sky, Tint blue), with center disc containing flywheel_center copy }
      - { name: legend,   type: 5 rows with color swatch + mono numeral + force name (use brand.flywheel_forces verbatim) }

  - id: 16_timeline
    name: Timeline
    surface: paper
    slots:
      - { name: titlebar, type: clean with eyebrow + H2 + lede }
      - { name: timeline, type: thin horizontal line with 5 circle markers, year labels in mono below, content cards alternating above and below }

  - id: 17_donut_pair
    name: Donut chart pair
    surface: split (navy panel + paper)
    slots:
      - { name: panel,  side: left,  type: navy with H2 + body }
      - { name: donuts, side: right, count: 2, style: thin stroke (8% width), big % in center (Inter Tight 700), mono caption below }

  - id: 18_bar_area
    name: Bar + area chart pair
    surface: paper
    slots:
      - { name: titlebar, type: clean with eyebrow + H2 }
      - { name: chart_left,  type: clustered bar chart, 3 series, colors: [Sky, Navy, Blue] }
      - { name: chart_right, type: stacked area chart, 2 series, colors: [Sky 55% opacity, Blue 85% opacity] }
      - { name: legends,     type: mono small with circle swatches }

  - id: 19_comparison_matrix
    name: Comparison matrix
    surface: paper
    slots:
      - { name: titlebar, type: clean with eyebrow + H2 + short lede }
      - { name: table,    type: 4-column hairline grid, header row underlined with 2px navy, row labels in Inter Tight 600 left-aligned, cells: success_check or risk_cross icons (1.7cqw circles with semantic tinted bg) }

  - id: 20_brand_notes
    name: Brand notes (style reference)
    surface: paper
    slots:
      - { name: titlebar, type: clean }
      - { name: typesample, type: 5 rows: Display / H2 / H3 / Body / Mono with mono key on left + actual sample on right }
      - { name: palette_row, type: brand swatches (5) + semantic swatches (5) }
      - { name: rules,    type: 4 short bullet rules }

  - id: 21_logos_icons
    name: Logos & icon library
    surface: split (paper left + navy right)
    slots:
      - { name: logos, side: left,  type: 4-tile grid (wordmark light, wordmark dark, symbol light, symbol dark) }
      - { name: icons, side: right, type: 12-icon grid on navy with thin 1px white-12% borders, 1.4 stroke }

  - id: 22_product_photos
    name: Product photos
    surface: paper
    slots:
      - { name: titlebar, type: clean }
      - { name: bento,    type: 5-card mockup grid in 3 columns, contains: real-feeling device frames (laptop / phone / monitor) with stylized Foley UI inside (KPI numbers in Inter Tight, mono captions, thin progress rings, success pills) }

voice:
  sounds_like:
    - "Hire in days, not weeks."
    - "Get your fleet to clear — and keep it there."
    - "Foley surfaces the signals. Navigator explains what they mean."
    - "From 5 drivers to 500, one platform."
  does_not_sound_like:
    - "Revolutionary, world-class, best-in-breed solutions."
    - "Leveraging synergies to drive compliance excellence."
    - "YOUR #1 PARTNER!!!"
    - "Click here to learn more."
  rules:
    - "Second person: 'you', 'your fleet'. Not 'our customers'."
    - "Sentences ≤ 18 words. One idea per sentence."
    - "Tabular numerals (write '42%', not 'forty-two percent')."
    - "Concrete CTA verbs: 'Book a demo', 'See pricing', 'Talk to compliance'. Never 'Learn more' alone."
    - "Sentence case for headlines. No marketing-style Title Case."

self_check:
  - Zero ALL CAPS headlines (eyebrow/mono labels only, ≤12 px)
  - Foley Blue is the only brand accent. Green is only "cleared" status.
  - The supplied Foley logo is used unmodified — never redrawn or recolored
  - Every slide answers exactly one question
  - ≤5 bullets per slide, ≤3 sentences per paragraph
  - One photo OR one UI shot per slide (never both)
  - Foley wordmark + slide counter on every slide
  - Closing slide has a concrete CTA verb, not "Thank you"
  - No "Foley Services" / "Foley Carrier Services" anywhere

```

---

## 2. Generation prompt

> Paste the block below into Gamma's "Generate a presentation" field (or equivalent in Tome / Beautiful.ai / Pitch AI). The schema above defines the rules; this prompt drives the content.

```
You are creating a modern executive presentation for Foley (foley.io) — a 30-year compliance, safety, and screening platform for commercial fleets in North America. The deck goes to investors, banks, executive partners, and large prospects, so the visual bar is tier-1 SaaS (think Stripe, Linear, Anthropic), not a corporate template.

The brand spec for this deck is in the attached `foley-deck-config.yaml`. Treat it as binding. Pick layouts only from the 22 listed there. Use the exact palette tokens, the exact typography, the supplied Foley logo. Use the brand's voice rules. Run the self_check before finishing.

Photography direction: documentary editorial of real fleets, drivers, depots, dispatch rooms — never staged stock handshakes, never abstract gradients in place of imagery. Apply a navy tonal overlay over hero photos so titles in white remain legible.

Charts: Swiss minimal. Foley Blue as the primary series color, Muted grey dashed for benchmarks. Tabular mono labels on axes, hairline grid lines. No multicolor pie charts.

Density rule: each slide answers exactly one question. If you can't articulate the question, cut the slide.

CONTENT BRIEF — replace this section per use case
==================================================

Audience:        VP of Safety / COO at a 200–500 truck fleet
Length:          22 slides, ~35-minute meeting
Goal:            book a demo and pilot CSA Monitoring + Hiring + Navigator AI
Date:            May 2026

Slide order (mapped to layouts in the YAML schema):

  01_cover                  Smarter data. Lower risk. Safer fleets.
  02_cover_contact          Briefing context — May 2026, contacts
  03_section_photo          01 · The compliance reality
  06_title_photo_cards      Three problems we kept hearing
  09_title_2cards           Two systems compared
  04_section_navy           02 · The Foley platform
  10_title_3cards           Three signal classes (CSA, Hiring, Navigator)
  11_title_4cards           Four product surfaces (CSA · Hiring · Background · Navigator AI)
  07_title_3numbered        How CSA Monitoring works in 3 steps
  08_4numbered_panel        Hiring flow in 4 steps
  12_quadrants              Four areas of the platform
  17_donut_pair             Audit risk −42%, DQ completeness 98.4%
  18_bar_area               12-month outcomes (bar + area)
  19_comparison_matrix      Foley vs. legacy stack
  03_section_photo          03 · Customer voice
  13_social_proof           4 testimonials
  14_photo_collage          Industries served (bento)
  15_flywheel               The Foley Flywheel
  16_timeline               Roadmap 2021 → Soon
  20_brand_notes            (internal only — drop for external)
  21_logos_icons            (internal only — drop for external)
  22_product_photos         Product surfaces preview

For external decks: drop slides 20 and 21 and renumber.

Photography keywords for each slide that needs imagery (use these to source/generate visuals):
  01_cover         "highway aerial top-down, freight trucks, dawn, navy tonal grade"
  02_cover_contact "semi truck driver portrait in cab, candid, natural light"
  03_section_photo "fleet of trucks in depot, wide angle, slight blue grade"
  05_agenda        "truck dashboard / steering wheel, candid, shallow DOF"
  06_title_photo_cards  3x circle portraits: "Director of Safety", "Recruiter at fleet", "Compliance lead"
  14_photo_collage 5x bento: "truck on highway", "depot at dusk", "aerial road", "driver portrait", "warehouse crew"

End of brief.
```
