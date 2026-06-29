# Kingdom of Heaven Embassy — Design Brief

## Tone
Governmental, constitutional, transformational. Premium digital embassy with celestial depth and legal authority — not corporate, not educational, not commercial.

## Palette
| Token | OKLCH | Usage |
|-------|-------|-------|
| Background | 0.12/0.18/250 | Primary royal blue dark base |
| Primary Accent | 0.80/0.18/70 | Gold — seals, badges, CTAs, highlights |
| Card | 0.15/0.18/250 | Elevated surfaces with subtle depth |
| Foreground | 0.98/0.02/45 | Off-white text, maximum contrast |
| Muted | 0.20/0.15/250 | Secondary surfaces, citations |
| Destructive | 0.704/0.191/22.216 | Alerts, rejection states (restrained use) |

## Typography
| Layer | Font | Usage |
|-------|------|-------|
| Display | Fraunces | Constitutional headers, article numbers, crest text |
| Body | Lato | Body copy, UI labels, standard text |
| Heading | Playfair Display | Page titles, major section heads |
| Mono | Geist Mono | Legal citations, article references, code-style text |

## Shape Language
Rigid, structured, governmental. Minimal rounding (0.625rem default); sharp borders for legal documents. Left accent borders on cards (4px gold). Circular seals (50% border-radius). Vertical rules and dividers (thin, gold-tinted gradients).

## Structural Zones
| Zone | Appearance | Purpose |
|------|-----------|---------|
| Header | Seal badge with crest, governmental typography | Establish authority and identity |
| Main Content | Card-based grid with left borders | Department/feature organization |
| Constitution Gate | Full-width legal document styling, scroll-reveal | Onboarding transformation |
| Dashboard | 9 department cards in 3×3 grid, articles sections | Central navigation hub |
| Knowledge Vault | Archive-style items with icons, legal citations | Document/reflection storage |
| Media Library | Three media types (video, PDF, audio) in card grid with seal badges | Official embassy broadcast archive |
| Footer | Minimal, muted borders, citation-style text | Constitutional reference |

## Component Patterns
- **Department Cards**: Left 4px gold border, subtle shadow, hover lift (+2px), hidden grid icons
- **Seal Badges**: Circular, 3px gold border, radial gradient fill, centered icon
- **Article Sections**: Left border with numbered circle, progressive reveal animation
- **Knowledge Vault Items**: Left gradient accent bar (3rem × 1rem), flex layout, citation text
- **Media Cards**: Left 4px gold border, play/document overlay on hover, lift (+2px), three variants (video, PDF, audio)
- **Podcast Player**: Minimal linear design, gold progress bar, circular play buttons, time display
- **PDF Viewer**: Bordered frame with page navigation buttons (gold primary), page counter
- **Buttons**: Gold primary, royal blue text; secondary uses royal blue border on transparent
- **Legal Dividers**: Thin horizontal rule with gold gradient (fade in/out)

## Motion
- **Celestial Base**: Stars twinkle (20s loop), shimmer text on display heads (3s loop), float effect (6s loop) — all inherited from existing codebase
- **Constitutional Reveals**: Article sections fade-in with slide-up (0.6s ease-out, staggered by order)
- **Seal Spin**: Subtle 360° rotation (8s linear, infinite) for interactive seals or progress indicators
- **Department Hover**: 2px lift on card, shadow intensification, left border color shift to primary gold

## Signature Detail
**Governmental Seal Integration**: Every major interface section opens with a circular seal badge (gold border, royal blue gradient fill). Text inside seal uses Fraunces (constitutional serif). Seal spins slowly on dashboard load — visual metaphor for "entering the embassy."

## Media Library Specification
**Purpose**: Official Embassy media archive and broadcast center — visitors get sample content (one video, one PDF, one podcast), citizens+ access full library. Three media types: Video (📹), PDF (📄), Audio (🎙️).

**Components**: Media cards (left 4px gold border, hover overlay with gold play/document icon, lifts +2px). Video uses html5 `<video>`. PDF viewer has page navigation buttons and counter. Podcast player is minimal linear (gold progress bar, circular play button 3rem). Section header "II. Kingdom Broadcast Center" uses Fraunces serif, 1.5rem, gold underline. Grid: 3-column (300px min), auto-fill responsive, 1.5rem gap. No new animations — reuse `reveal-article`.

## Anti-Patterns (What We Reject)
- Rounded corners on critical governmental UI (seals, badges, cards remain sharp or circular)
- Bright, cheerful colors — this is not celebratory, it is transformational and serious
- Generic placeholder shadows — custom shadows use embassy-specific color range and blur
- Scattered animations without choreography — all motion serves governmental state changes
- Rainbow or overly-saturated palettes — only royal blue, gold, and neutral off-white

## Constraints
- Always use OKLCH tokens; never raw hex or named colors
- Maintain minimum 0.7 L (lightness) difference for foreground-on-background
- Department cards must have left accent border (never top or full-frame)
- Seals must be circular (50% border-radius)
- Legal citations use Geist Mono, never Arial or system fonts
- Constitution gate must block dashboard access (browser-level guard, not just hidden)

