# YOU LI — Design System Documentation

**Concept name:** *Material Intelligence in Motion*
**Industry:** B2B textile sourcing / fabric supply (China-to-Bangladesh corridor)
**Research date:** 10 September 2026

---

## 1. Industry design research (what “luxury” means in this sector)

Findings from current (2025–2026) luxury B2B / fashion-industry design research, synthesized:

| Research signal | Implication for YOU LI |
| --- | --- |
| **Near-black / deep-navy dark-mode-first palettes** are the dominant luxury formula (dark mode now specified in ~30% of new luxury web projects; Bottega Veneta, Chanel run near-monochrome dark bases with ≤3 active colors). Avoid pure `#000`. | Deep ink navy `#0C1B2A` base for hero/CTA/footer bands; warm ivory `#F6F3EE` ground — never pure white/black. |
| **One anchor color + one or two restrained metallic accents.** Champagne/bronze gold over dark; muted, warmed, never saturated primaries. | Bronze `#B0823F / #C58B3A` as the single accent (CTAs, indices, hairlines), teal `#2F7C7A` reserved for “verified/tested” semantic states. |
| **Bold yet understated typography:** high-contrast custom serifs (Canela/Bodoni-class) for display; ultra-clean sans for UI; luxury sites pair an editorial serif with a neutral sans. | **Fraunces** (high-contrast, optical-size display serif) + **Manrope** (neutral modern sans) + **IBM Plex Mono** for the technical/data layer (GSM, cert IDs, evidence labels) — the “mill ledger” texture. |
| **Quiet luxury minimalism:** generous negative space, hairline rules, a single bold focal element per screen; oversized serif statements. | 96px section rhythm, 1px hairline dividers everywhere, numbered section indices, one hero statement per screen, no decorative clutter. |
| **Digital-tactile texture:** subtle grain, material-mimicking surfaces; fashion houses lean on macro fabric photography. | Raking-light macro fabric photography (conceptual, labeled) on every category; a faint woven-line gradient texture in dark bands; real swatch-style imagery in cards. |
| **B2B buyers expect conservative, legible, data-first layouts** — luxury here is *precision*, not ornament. | The **evidence-status pill system** (Verified document / Company statement / Reference range / Verification in progress / Buyer permission required / Not publicly verified) is rendered as a first-class visual component — the differentiator, not a footnote. |

**Positioning of the visual language:** *fashion-house editorial* (serif, ivory, bronze, macro texture) × *mill-floor technical* (monospace data, spec tables, evidence codes). The two never fight: serif owns the narrative, mono owns the data.

## 2. Tokens

### Color
| Token | Hex | Role |
| --- | --- | --- |
| `--ink` | `#0C1B2A` | Primary dark ground (hero, CTA, footer) |
| `--ink-2` | `#102A43` | Dark surface |
| `--ivory` | `#F6F3EE` | Page ground (never pure white) |
| `--paper` | `#EFEAE1` | Alternate section ground |
| `--graphite` | `#25313B` | Body text |
| `--slate` | `#5C6B78` | Secondary text |
| `--bronze` / `--bronze-2` | `#B0823F` / `#C58B3A` | Single accent: CTAs, indices, rules, hover |
| `--teal` | `#2F7C7A` | Verified / tested / positive semantic |
| `--amber` | `#B7791F` | Review-needed / in-progress semantic |
| `--hairline` | `rgba(16,42,67,.16)` | Dividers on light |
| `--hairline-d` | `rgba(246,243,238,.16)` | Dividers on dark |

Contrast: all text pairs verified for WCAG AA on their ground (bronze is used on dark grounds and as a rule color; body text is graphite/ink).

### Typography
| Role | Face | Sizes |
| --- | --- | --- |
| Display (H1/H2, card names) | Fraunces (300–600, opsz) | H1 `clamp(38px,4.6vw,62px)`, H2 `clamp(26px,2.6vw,36px)` |
| UI / body | Manrope (300–700) | Body 17/1.65; UI 13.5–15 |
| Data / labels | IBM Plex Mono (400/500) | Eyebrows 11.5/.22em; pills 10/.08em; chips 10.5 |

### Spacing & grid
- 8px base scale; section rhythm 96px desktop / 56px mobile.
- 12-column-equivalent container, max-width 1280px, 28px gutters (20px mobile).
- Cards: 22px gaps or 1px hairline-grid (the “ledger” look).

## 3. Signature components

1. **Evidence pill** — six states, mono-caps, hairline border. The site’s core trust component; appears on every claim (spec tables, product cards, FAQ answers, certifications register).
2. **Spec table** — hairline-ruled, mono headers, pill in the status column; the “ledger” row pattern.
3. **Numbered section heads** — mono index (`01`–`10`) + serif H2 over a top hairline; editorial structure made visible.
4. **Product card** — macro category imagery under a dark gradient, serif name, mono spec chips, evidence pill, dual action (full record / request specification).
5. **Mega-menu** — full-width six-group panel for Products; right-aligned dropdowns for edge items; hover + click + keyboard.
6. **Dark CTA band** — ink ground with a radial teal/bronze glow and woven-line texture; primary CTA is always `Request a Fabric Match`.
7. **Split blocks** — serif copy left, framed imagery right with a “conceptual imagery” caption (AI-visual disclosure per strategy brief §21).
8. **Steps / route grid** — numbered, hairline-divided, with an *owner* line per step (the process is a product).

## 4. Motion & accessibility
- Reveal-on-scroll (IntersectionObserver, 18px/600ms) — disabled under `prefers-reduced-motion`.
- Hover micro-motion: card lift 3px + shadow, arrow nudge, image scale 1.045 — all ≤300ms.
- 44px minimum touch targets; visible bronze focus rings; keyboard-navigable menus and accordions (native `<details>` for FAQs); semantic HTML5 landmarks; one H1 per page.
- Performance: zero frameworks, one CSS file, one JS file (~10KB), fonts via Google Fonts with system fallbacks, lazy-loaded below-fold imagery.

## 5. Imagery policy (per strategy brief §21)
- All imagery is **conceptual (AI-generated)** and captioned as such on-site; it never depicts real YOU LI factories, offices, people, clients or certificates.
- Macro fabric textures carry the category identity; inspection/office scenes carry the process narrative.
- No stock factory imagery, no competitor logos, no client logos (permission gate per brief §10/§25).
