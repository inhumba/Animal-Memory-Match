---
name: Animal Memory Match
description: Playful, warm memory game for kids — emoji cards, canvas craft, encouraging UI
colors:
  primary: "#4f46e5"
  primary-deep: "#4338ca"
  primary-light: "#818cf8"
  primary-surface: "#eef2ff"
  primary-border: "#c7d2fe"
  sky-wash: "#f0f4ff"
  surface-white: "#ffffff"
  surface-glass: "rgba(255, 255, 255, 0.8)"
  accent-sunrise: "#facc15"
  accent-coral: "#fb923c"
  accent-pink: "#ec4899"
  accent-emerald: "#34d399"
  accent-teal: "#14b8a6"
  stat-pink-bg: "#fce7f3"
  stat-pink-ink: "#db2777"
  stat-teal-bg: "#ccfbf1"
  stat-teal-ink: "#0d9488"
  stat-amber-bg: "#fef3c7"
  stat-amber-ink: "#d97706"
  victory-gold: "#eab308"
  overlay-deep: "rgba(30, 27, 75, 0.75)"
  ink-strong: "#312e81"
  ink-muted: "#818cf8"
typography:
  display:
    fontFamily: "Margarine, cursive"
    fontSize: "clamp(1.5rem, 5vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "0.025em"
  headline:
    fontFamily: "Margarine, cursive"
    fontSize: "clamp(1.25rem, 4vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "0.025em"
  title:
    fontFamily: "Margarine, cursive"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "normal"
  body:
    fontFamily: "Quicksand, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 700
    lineHeight: 1.5
    letterSpacing: "normal"
  label:
    fontFamily: "Quicksand, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.05em"
rounded:
  sm: "12px"
  md: "16px"
  lg: "24px"
  full: "9999px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "16px"
  lg: "24px"
  xl: "48px"
components:
  button-play:
    backgroundColor: "linear-gradient(90deg, #facc15, #fb923c, #ec4899)"
    textColor: "#ffffff"
    typography: "{typography.display}"
    rounded: "{rounded.full}"
    padding: "12px 48px"
  button-play-hover:
    backgroundColor: "linear-gradient(90deg, #eab308, #f97316, #db2777)"
    textColor: "#ffffff"
    rounded: "{rounded.full}"
    padding: "12px 48px"
  button-action:
    backgroundColor: "linear-gradient(90deg, #34d399, #14b8a6)"
    textColor: "#ffffff"
    typography: "{typography.title}"
    rounded: "{rounded.sm}"
    padding: "10px 16px"
  button-ghost:
    backgroundColor: "#e0e7ff"
    textColor: "#4338ca"
    typography: "{typography.title}"
    rounded: "{rounded.md}"
    padding: "14px 20px"
  theme-card:
    backgroundColor: "#eef2ff"
    textColor: "#4338ca"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "12px 16px"
  theme-card-active:
    backgroundColor: "rgba(224, 231, 255, 0.8)"
    textColor: "#4338ca"
    rounded: "{rounded.md}"
    padding: "12px 16px"
---

# Design System: Animal Memory Match

## 1. Overview

**Creative North Star: "The Encouraging Playroom"**

Animal Memory Match looks and feels like a bright, patient playroom where a child can explore at their own pace. The HTML shell handles navigation, setup, and celebration; the canvas handles the tactile card game with procedural gradients, particles, and speech. Visual energy comes from emoji, rounded shapes, and saturated accent moments—not from stacking every kids-app trope at once.

The system is warm and playful without becoming corporate edtech. PRODUCT.md rejects generic "AI kids app" aesthetics (pastel gradient washes, identical bubbly card grids, glassmorphism headers, rainbow gradient CTAs on every screen). Future polish should sharpen craft in the canvas and typography while shedding reflex patterns that make the shell feel templated.

**Key Characteristics:**

- **Dual-surface architecture:** Tailwind HTML for menus/HUD; canvas for cards, particles, and theme-specific card-back gradients.
- **Indigo spine + rainbow accents:** Indigo-600 anchors navigation and copy; pink/teal/amber stat pills and per-theme canvas gradients add color in controlled bursts.
- **Bubbly but tappable:** Generous `rounded-2xl`/`rounded-3xl` radii, `border-4` outlines, and `active:scale-95` press feedback for small fingers.
- **Encouragement-first copy:** Margarine display voice for headlines; Quicksand bold for body. Uppercase reserved for short HUD labels (Flips, Pairs Left).
- **Depth via shadow + blur, not flat cards only:** `shadow-xl`/`shadow-2xl` on panels; selective `backdrop-blur` on overlays—not decorative glass everywhere.

## 2. Colors

A soft indigo-lavender sky wash carries the page; saturated accents appear on CTAs, stat pills, difficulty chips, and canvas card backs.

### Primary

- **Adventure Indigo** (#4f46e5): Headlines, theme labels, canvas name badges, active ring accents. The structural voice of the UI.
- **Deep Indigo** (#4338ca): Selected theme text, victory stat values, stronger emphasis on setup headings.
- **Whisper Indigo** (#818cf8): Subtitles, footer copy, muted instructional text.

### Secondary

- **Sunrise Gradient** (#facc15 → #fb923c → #ec4899): Primary play CTA ("Let's Play!") and victory "Play Again" button. One hero moment per screen—never repeated on every control.
- **Fresh Meadow** (#34d399 → #14b8a6): New Game action button. Signals "start over" without competing with the play CTA.

### Tertiary

- **Stat Pink** (#fce7f3 bg / #db2777 ink): Flips counter HUD pill — visible during play.
- **Stat Teal** (#ccfbf1 bg / #0d9488 ink): Pairs Left HUD pill — visible during play.
- **Stat Violet** (score pill): Round score out of 100 — hidden during play; revealed on victory.
- **Stat Amber** (#fef3c7 bg / #d97706 ink): Best score HUD pill — visible on menu; hidden during play; shown again on victory.
- **Difficulty hues:** Green (#f0fdf4 / #15803d), amber, rose, purple—each difficulty tier gets its own pastel pair, not shared indigo.

### Neutral

- **Sky Wash** (#f0f4ff): Body fallback and scrollbar track. Page gradient runs indigo-100 → purple-50 → pink-100.
- **Cloud White** (#ffffff): Setup panel, game board frame, victory card, card faces on canvas.
- **Indigo Mist** (#eef2ff / #e0e7ff / #c7d2fe): Theme card backgrounds, stat summary panels, borders.
- **Overlay Dusk** (indigo-950 at 75%): Victory modal scrim.

### Named Rules

**The One Rainbow Rule.** A full yellow-orange-pink gradient is reserved for the primary play path (Let's Play, Play Again). Secondary actions use solid or two-stop gradients (emerald-teal, indigo tints). If every button is a rainbow, none of them are special.

**The Canvas Color Rule.** Theme-specific card-back gradients live on the canvas only. The HTML shell stays on the indigo spine so setup doesn't become 12 competing palettes.

## 3. Typography

**Display Font:** Margarine (cursive, Google Fonts)
**Body Font:** Quicksand (weights 500, 700, Google Fonts)

**Character:** Margarine gives headlines a hand-drawn, storybook warmth; Quicksand keeps labels and instructions crisp and legible at small sizes. The pairing says "playful teacher," not "startup dashboard."

### Hierarchy

- **Display** (400, clamp 1.5rem–3rem, line-height 1.1): Page title "Animal Match", setup hero "Choose Your Adventure!", play CTA.
- **Headline** (400, clamp 1.25rem–3rem, line-height 1.1): Victory "Amazing Job!", section prompts on setup.
- **Title** (400, 1.125rem, line-height 1.2): Section eyebrows ("Theme Category", "Match Difficulty"), button labels in Margarine.
- **Body** (700, 0.875rem, line-height 1.5): Theme/difficulty button text, footer hints, victory stat values.
- **Label** (700, 0.75rem, uppercase, tracking 0.05em): HUD counters (Flips, Pairs Left, Best Score), victory subhead.

### Named Rules

**The Two-Voice Rule.** Margarine is for moments of delight (titles, CTAs, scores). Quicksand is for reading and scanning (instructions, stats, footer). Never set body paragraphs in Margarine.

## 4. Elevation

This system uses a hybrid: soft diffuse shadows on panels plus tonal layering (white surfaces on gradient sky) and selective backdrop blur on overlays. Canvas cards add their own micro-shadow (`rgba(99, 102, 241, 0.15)`, blur 12px, offset 4px).

Depth is structural, not decorative. Floating panels (header, setup, victory) lift; flat stat pills inside the header sit one level down with `border-2` instead of heavy shadow.

### Shadow Vocabulary

- **Panel lift** (`shadow-xl`): Header bar, setup screen container.
- **Hero lift** (`shadow-2xl`): Game board frame, play CTA, victory card.
- **Control nudge** (`shadow-md`): Theme cards, difficulty chips, secondary buttons.
- **Icon rest** (`shadow-sm`): Audio toggle at rest.

### Named Rules

**The Blur-With-Purpose Rule.** `backdrop-blur` appears on the header (80% white), setup overlay (95% white), and victory scrim—not on every child element. If blur doesn't separate layers, remove it.

## 5. Components

### Buttons

- **Shape:** Generously rounded—`rounded-xl` (12px) for actions, `rounded-full` for the hero play CTA.
- **Primary (Play):** Sunrise gradient, white Margarine text, `border-4 border-white`, `shadow-2xl`, hover `scale-105`, active `scale-95`.
- **Action (New Game):** Emerald-to-teal gradient, white text, `border-2 border-emerald-300`.
- **Ghost (Back to Menu):** `#e0e7ff` background, `#4338ca` text, `rounded-2xl`, `shadow-md`.
- **Icon (Audio):** `#e0e7ff` fill, `#4f46e5` stroke icon, square `p-2.5`, no text label on mobile.

### Chips

- **Difficulty chips:** `rounded-2xl`, `border-4`, pastel bg matching tier (green/amber/rose/purple), bold Quicksand label. Active state: darker border + `ring-4` in matching hue.
- **HUD stat pills:** `rounded-xl`, `border-2`, tier-specific pastel bg. Label in uppercase label typography; value in Margarine at `text-xl`–`text-2xl`. **During play:** only Flips + Pairs Left. **After victory:** Score + Best join the header; numeric score also appears on the victory card (`XX / 100`).

### Cards / Containers

- **Setup panel:** White 95% + blur, `rounded-3xl`, `border-4 border-indigo-200`, `shadow-2xl`, scrollable on mobile.
- **Theme selector cards:** `rounded-2xl`, `border-4 border-indigo-100`, `bg-indigo-50`, large emoji (`text-4xl`–`text-5xl`). Active: `border-indigo-500`, `ring-4 ring-indigo-300`.
- **Game board frame:** White, `rounded-3xl`, `border-4`/`border-8 border-indigo-400/90`, `aspect-[4/3]`, hidden on `max-md` (mobile plays in canvas overlay flow).
- **Victory card:** White, `rounded-3xl`, `border-4 border-yellow-400`, centered stats panel in `bg-indigo-50`.

### Inputs / Fields

No text inputs in v1. Selection is entirely button/chip based.

### Navigation

Single-page flow: persistent header HUD during play (Flips + Pairs Left only), setup overlay for configuration, victory modal for completion and final score. Footer is informational only ("Made with 💖 for happy kids").

### Memory Card (Canvas)

- **Shape:** `radius: 16` drawn via quadratic curves; 3D flip via `flipProgress`.
- **Face:** White or mint-green when matched; inner `border-4` decorative stroke; emoji at 42% min dimension; Quicksand name badge below.
- **Back:** Per-theme two-stop linear gradient (e.g. safari: amber → pink). Unique per theme category, not per HTML shell color.
- **Matched state:** Green check badge, gentle pulse animation, mint badge background.

## 6. Do's and Don'ts

### Do:

- **Do** keep the indigo spine consistent across setup, HUD, and victory so the shell feels like one game, not twelve separate themes.
- **Do** use Margarine only for delight moments and Quicksand for scannable text.
- **Do** give every tappable control `active:scale-95` and a minimum touch target of ~44px.
- **Do** reserve the sunrise gradient CTA for the primary forward action on each screen.
- **Do** put theme-specific color energy on canvas card backs where it reinforces the chosen adventure.

### Don't:

- **Don't** use generic "AI kids app" aesthetics: soft pastel gradient backgrounds on every surface, identical bubbly card grids, glassmorphism headers, and rainbow gradient CTAs stacked on every screen.
- **Don't** add corporate edtech dashboards with badges, streaks, or "learning platform" framing.
- **Don't** create overstimulating sensory overload: too many simultaneous animations, sounds, and competing accent colors.
- **Don't** put a rainbow gradient on every button—one hero CTA per view.
- **Don't** add `backdrop-blur` decoratively to elements that don't separate layers.
- **Don't** use uppercase for body copy or sentences—reserve it for HUD labels ≤4 words.
