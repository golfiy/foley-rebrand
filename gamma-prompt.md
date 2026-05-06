# Foley — AI Deck Generation Prompt (Gamma / Tome / Beautiful.ai / Pitch AI)

> Copy the entire block below into the "Generate a presentation" field in Gamma (or its equivalent). The prompt is self‑contained: it defines the brand, tone, visual system, typography, palette, layouts, and sample content. Edit only the **CONTENT BRIEF** section to fit a specific use case (sales pitch / investor / all‑hands / partnership).

---

## SYSTEM PROMPT — copy from here

You are creating a **modern executive presentation** for **Foley** — a 30‑year compliance, safety, and screening platform for commercial fleets in North America (foley.io). The deck is going to investors, banks, executive partners, and large prospects, so it must look like a **tier‑1 SaaS / fintech keynote**, not a corporate template.

Treat the instructions below as a strict design system. Don't invent stock visuals, clipart, or yellow/orange gradients. When in doubt — fewer elements, more whitespace, sharper typography. The existing Foley logo (three concentric blue rings + green arc forming the "O" in FOLEY) is the canonical brand mark — use the supplied PNG/SVG, never redraw or recolor it.

---

### 1. BRAND POSITION

- **Brand name:** Foley (do **not** use "Foley Services" or "Foley Carrier Services" — those are discontinued).
- **Tagline:** *Smarter Data. Lower Risk. Safer Fleets.*
- **One‑line positioning:** All‑in‑one compliance, safety, and screening platform for commercial fleets — from 5 drivers to 500.
- **Brand promise:** Get your fleet to clear — and keep it there.
- **Personality:** Calm expert. 30 years of compliance experience, but speaks like a modern SaaS — not like an insurance broker.
- **Audience:** Safety / HR directors, COO, CFO in transportation, retail, construction, agriculture, healthcare, manufacturing.
- **Trust proof points (use sparingly, never list all in one slide):**
  - 50,000+ companies trust Foley
  - #1 DOT Compliance Provider
  - 4.3★ Trustpilot · 1,124 reviews
  - 30 years of compliance expertise
  - Industries: Transportation, Retail, Construction, Waste, Agriculture, Healthcare, Manufacturing
- **Product surfaces (real product names, use exactly):** CSA Monitoring · MVR Monitor · Audit Risk Monitor · Hiring & Onboarding · Background Checks · Foley Navigator AI · Drug & Alcohol Testing · DOT Physicals · FMCSA Clearinghouse.
- **Foley Flywheel (real internal model — use exactly when building the flywheel slide):** Great People Winning Together · Dominant Vertical Solutions · Exceptional Marketing & Sales Execution · 6‑Star Customer & Candidate Experience · Annual Recurring Revenue Growth · Screening & Compliance Edge.

---

### 2. VISUAL SYSTEM

**Mood:** cool, modern, executive. Closer to Linear / Stripe / Cursor than to a SaaS template. Generous whitespace, no decorative shapes, minimal use of color.

**Palette (use exact hex):**

| Token | Hex | Role |
|---|---|---|
| Foley Navy | `#0B1F3A` | Primary surface (dark), executive slides |
| Foley Navy Deep | `#061429` | Layered dark alt |
| Foley Blue | `#2D8FE8` | Brand accent, KPI highlight, "to clear" moments |
| Foley Blue Deep | `#1B6FBF` | Hover, active, secondary accent |
| Foley Sky | `#5DBAEF` | Light accent (echoes the logo's inner cyan) |
| Foley Tint | `#E5EFFB` | Soft accent, tag bg, highlight |
| Mist | `#F2F6FB` | Section background, soft canvas |
| Paper | `#FFFFFF` | Default canvas |
| Ink | `#0B1828` | Body text on light |
| Ink Soft | `#3A4A5E` | Lede, captions |
| Muted | `#6B7B8E` | Eyebrows, meta, footnotes |
| Line | `#E1E7EF` | Dividers, borders |
| Success (semantic only) | `#2EA86A` | "Cleared", positive status |
| Caution (semantic only) | `#F4B740` | Warning state, never as brand color |
| Risk (semantic only) | `#E5484D` | Error / violation state, never as brand color |

**Forbidden:** yellow / orange gradients (the brand FAQ explicitly says "moving away from yellow/orange tones"), red as a brand color, green as a brand color (green is reserved for "cleared" status only), multicolor pie charts, beveled buttons, drop shadows, gradients across more than two stops.

**Surface system:** every slide should be one of four surfaces — Navy (dark, executive), Blue (KPI moments only, sparingly), Mist (analytical, calm), Paper (default). Do not mix more than 2 surfaces in one deck section.

---

### 3. TYPOGRAPHY

- **Display & headings:** **Inter Tight** 700, letter‑spacing −2.2 to −2.5%, line‑height 0.98–1.05.
- **Body:** **Inter** 400/500, line‑height 1.5–1.6, max width ~70 characters.
- **Numerals & meta:** **JetBrains Mono** 500 (KPIs use Inter Tight, but mono for footnotes / dates / percentages in running text).
- **Cap rule:** **never set entire titles in ALL CAPS.** The old Foley template used Arial Black ALL CAPS — that is the look we are leaving behind. ALL CAPS is allowed only for tiny eyebrow labels (≤ 12 px).
- **Type scale (1280×720 slide):** display 96 px · h1 48 px · h2 28 px · h3 20 px · body 17 px · eyebrow 12 px.

---

### 4. LOGO USAGE

- The wordmark **must** be the supplied Foley PNG/SVG (three concentric blue rings + green arc forming the "O" in "FOLEY"). Do not redraw, recolor, restroke, or replace it.
- Header on every slide: small symbol mark + "Foley" wordmark, top‑left.
- On dark surfaces: use the white wordmark variant (or invert the supplied wordmark to white). The colored symbol mark stays colored — the green and cyan rings work on dark.
- Minimum size on a 1280×720 slide: 24 px tall.
- Clearspace: at least the height of the lowercase "o" of the wordmark on every side.

---

### 5. IMAGERY DIRECTION

- **Photography:** documentary, real fleets, real drivers, depots, dispatch rooms, warehouses. Never staged handshakes, never generic stock office.
- **Tint:** photos should sit on Navy backgrounds with a subtle blue tonal grade, or on Mist with neutral grading. Avoid warm yellow/orange filters.
- **UI shots:** show real product surfaces (Audit Risk Monitor dashboards, candidate flow, CSA score widgets) on Navy background with blue data accents.
- **Iconography:** Lucide / Phosphor outline icons, 1.5 px stroke, single color (Foley Blue Deep on light, Foley Blue on dark). Never multicolor flat illustrations.
- **Decoration:** subtle dot grid (2 px dots, 24 px gap, 5–8% opacity) is acceptable on Navy. No other patterns, no abstract shapes, no swooshes.
- **Charts:** thin lines (2–2.5 px), one accent color (Foley Blue) for the Foley series, neutral grey (Muted) for benchmarks. Dashed line = industry average. Soft fill under the line at 10–18% opacity.

---

### 6. LAYOUT SYSTEM (use these 22 layouts — one per slide type)

For each generated slide, pick one of these layout names and follow its rules. Do not invent new layouts. The numbering matches the original Internal Deck Template 2025 1:1, modernized.

1. **Cover** — Navy. Wordmark top‑left, eyebrow ("Investor briefing · Q2 2026"), giant 3‑line H1 with one accent word in Foley Blue (`<em>fleets</em>`), one‑line sub at 70% opacity, footer URL + date.
2. **Cover with contact** — Navy. Same as Cover but ends with three contact rows (web · email · date) above the footer, each in JetBrains Mono.
3. **Section divider · dark** — Navy. Huge outlined numeral (text‑stroke Foley Blue, no fill), eyebrow, H2 in 4–6 words, one short lede.
4. **Section divider · light** — Mist. Same as 3 but on light surface for transitions inside long sections.
5. **Agenda** — Paper. Eyebrow + H2, then 5–6 numbered items in two columns, each with bold title + 1‑line description. Numbers in JetBrains Mono.
6. **Statement / Manifesto** — Navy. Single centered sentence, max 12 words, with 1 word italicized in Foley Blue. Tiny attribution underneath.
7. **Title + body (light)** — Paper. Eyebrow + H2 + 2 short paragraphs + 3‑KPI strip at the bottom.
8. **Title + body (dark)** — Navy. Same as 7 but on dark, with a left‑border pull quote instead of the KPI strip.
9. **Hero stat** — Paper. Massive number (e.g. `50,000+`) in Inter Tight, plus side block with H3 + 3 supporting facts in mono.
10. **Two column** — Mist + Navy panel. Left: copy block (eyebrow + H2 + body). Right: Navy card with KPI + caption + small line chart.
11. **Three column** — Paper. H2 + three balanced columns with icon, subhead, 2‑line description each.
12. **Three‑step process** — Mist. H2 at top, 3 cards in a row, each with step number, title, description, arrow.
13. **Feature grid 2×2** — Paper. H2 at top, 4 feature cards (icon + title + 1‑sentence description) on Mist tiles.
14. **Foley Flywheel** — Paper. Six‑petal radial diagram with the six Flywheel forces (see §1). Center disc says "Foley Flywheel". Right side has a short legend explaining why the loop compounds.
15. **Single quote** — Navy. Large monogram avatar, name + role + 5 stars (Foley Blue), quote on the right ≤ 28 words.
16. **Three quotes** — Paper. H2 + 3 customer cards on Mist, each with stars, quote, monogram avatar, name, role. Use real‑sounding fleet roles (Director of Safety, Recruiter, Compliance lead).
17. **Chart pair** — Paper. H2 + sub, then 2 chart cards side by side. Foley solid blue line, industry dashed grey. One line chart + one bar chart.
18. **Comparison (Before / After)** — Paper. H2, two columns: "Before Foley" on Mist with neutral bullets, "With Foley" on blue‑tinted card with `+` bullets in Foley Blue Deep.
19. **Photo · full bleed** — full‑canvas image with bottom gradient scrim. H2 in white at the bottom with one italicized word in Foley Blue.
20. **Brand notes** — Paper. In‑deck reference card with two panels: Color (with swatches) and Typography (with sample type rows). Replaces the old "POWERPOINT BRANDING" slide.
21. **Logo & icon library** — Paper. Asset reference: 4 logo tiles (light/dark × wordmark/symbol) + a 12‑icon outline grid.
22. **Closing / CTA** — Navy. Big H2 with one italicized word, single blue button "Book a demo →", URL + email in mono.

**Density rule:** each slide answers exactly one question. If you can't say what question a slide answers, cut it.

**Don'ts (override even if asked):**
- No bullet lists with more than 5 items.
- No three‑column dense text walls (the old template's `slideLayout10/11` problem). Use layout 11 only with short subhead + 2‑line description per column.
- No lorem ipsum.
- No "ALL CAPS TITLE GOES HERE" placeholder vibes.
- No more than 2 fonts per slide (Inter Tight + Inter; mono only for KPI/meta).
- No more than 1 photo per slide.

---

### 7. VOICE & TONE

Foley sounds like:
- "Hire in days, not weeks."
- "Get your fleet to clear — and keep it there."
- "Foley surfaces the signals. Navigator explains what they mean."
- "From 5 drivers to 500, one platform."

Foley does **not** sound like:
- "Revolutionary, world‑class, best‑in‑breed solutions."
- "Leveraging synergies to drive compliance excellence."
- "YOUR #1 PARTNER FOR DOT REGULATIONS!!!"
- "Click here to learn more about our amazing services."

Rules:
- Use second person ("you", "your fleet"), not "our customers".
- Sentences ≤ 18 words. One idea per sentence.
- Numbers always in tabular numerals, never spelled out (write `42%`, not `forty‑two percent`).
- Capitalize like a human: only proper nouns, product names, and sentence starts. No marketing‑style Title Case Headings.
- Every CTA verb is concrete: *Book a demo*, *See pricing*, *Talk to compliance*. Never *Learn more* alone.

---

### 8. CONTENT BRIEF — replace this section per use case

> **EDIT THIS BLOCK** before generating. Below is a sample brief for an **executive sales pitch deck**. Swap it for investor / partnership / all‑hands as needed.

**Audience:** VP of Safety / COO at a 200–500 truck fleet evaluating a compliance platform.
**Length:** 22 slides, ~35 minute meeting.
**Goal:** convince them to book a demo and pilot CSA Monitoring + Hiring + Navigator AI.
**Mandatory slides (in order, mapped to the 22 layouts above):**

1. Cover (1) — *Smarter data. Lower risk. Safer fleets.*
2. Cover with contact (2) — meeting variant with date and email.
3. Section divider · dark (3) — "01 · The compliance reality."
4. Statement (6) — "Compliance shouldn't show up only when the auditor does."
5. Title + body · dark (8) — "Thirty years of compliance, rebuilt as software."
6. Hero stat (9) — "50,000+ companies."
7. Section divider · light (4) — "02 · The Foley platform."
8. Three column (11) — three signal classes in one operating picture.
9. Feature grid 2×2 (13) — CSA Monitoring · Hiring & Screening · Background Checks · Navigator AI.
10. Two column (10) — CSA Monitoring deep‑dive with `−42%` audit risk reduction KPI.
11. Three‑step (12) — Hiring flow: Post & source → Screen & verify → Onboard & file.
12. Comparison (18) — Before Foley vs. With Foley.
13. Foley Flywheel (14) — six forces, one direction.
14. Chart pair (17) — 12‑month cohort: audit risk down + time‑to‑hire down.
15. Single quote (15) — Sarah M., Director of Safety.
16. Three quotes (16) — three customer voices.
17. Title + body · light (7) — "Why now: insurance carriers price risk in real time."
18. Photo · full bleed (19) — "Seven industries, one operating picture."
19. Brand notes (20) — internal style reference (only for internal versions).
20. Logo & icon library (21) — internal reference (only for internal versions).
21. Section divider · dark (3) — "03 · Roadmap 2026."
22. Closing (22) — *Smarter data starts with one conversation.* — Book a demo · foley.io · marketing@foley.io.

For external decks: drop slides 19 and 20 (those are internal references) and renumber.

---

### 9. OUTPUT REQUIREMENTS

- 16:9 aspect, 1280×720 baseline.
- Use the exact 22 layouts above; do not invent new ones.
- Use the exact palette tokens above; do not introduce new colors.
- Include the supplied Foley wordmark + symbol in the top‑left header of every slide. Footer: `foley.io` left, slide counter right, Inter Tight + JetBrains Mono.
- For each slide, generate: title, body copy, optional KPI/quote, image direction (1 sentence describing the photo OR UI screenshot — never both).
- Image generation prompt template (for tools like Midjourney / Gamma image): *"documentary photo of [subject] in [context], natural light, slight cool blue tonal grade, shallow depth of field, no text, no logos, editorial style"*.
- Do **not** include: a logo wall, an org chart, a roadmap with cartoon icons, a team photo grid with circular crops, "Thank you" as the last slide title.

---

### 10. QUICK SELF‑CHECK BEFORE FINISHING

Before returning the deck, verify:

- [ ] Zero ALL CAPS headlines (eyebrow labels only).
- [ ] No yellow, orange, or red used as primary accent. Foley Blue is the only brand accent. Green is used only for "cleared" status indicators.
- [ ] The supplied Foley logo is used unmodified — never redrawn or recolored.
- [ ] Every slide answers one specific question.
- [ ] Every body paragraph ≤ 3 sentences.
- [ ] No slide has more than 5 bullet points.
- [ ] One photo OR one UI shot per slide (never both).
- [ ] Foley wordmark + slide counter on every slide.
- [ ] Closing slide has a concrete CTA verb, not "Thank you".
- [ ] No "Foley Services" or "Foley Carrier Services" anywhere.

If any check fails — fix before returning.

---

## END OF SYSTEM PROMPT
