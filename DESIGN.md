```markdown
# Design System Document

## 1. Overview & Creative North Star: "The Kinetic Arena"
The Creative North Star for this design system is **"The Kinetic Arena."** 

This isn't a generic fitness app; it is a high-impact, editorial experience that mirrors the intensity, precision, and raw energy of the Michaelson Brothers MMA brand. We move away from the "safe" corporate grid by utilizing **Hard Brutalism**—defined by a strict 0px radius (no rounded corners), aggressive typography scales, and a monochromatic base punctuated by a lethal "Signal Red." 

The design breaks the standard template look through **intentional asymmetry**. Layouts should feel like they are in motion: utilize overlapping text elements, full-bleed imagery that breaks container boundaries, and a hierarchy driven by massive scale shifts. We aren't just presenting information; we are staging a confrontation.

---

## 2. Colors
Our palette is rooted in deep obsidian tones with high-contrast accents.

- **Primary (`#ffb4aa` / `#e21b1b`):** This is your "Signal Red." It is used sparingly but violently—for calls to action, critical highlights, and indicating active states.
- **Surface Hierarchy (The Foundation):**
    - **Background (`#131313`):** The canvas. A deep, ink-black.
    - **Surface Container Lowest (`#0e0e0e`):** Used for "recessed" areas like footer basements or input field backgrounds.
    - **Surface Container High (`#2a2a2a`):** Used to elevate secondary content cards or floating navigation.
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. We define space through tonal shifts. If a section ends, the background transitions from `surface` to `surface-container-low`.
- **The "Glass & Gradient" Rule:** To add "soul" to the darkness, use Glassmorphism for floating navigation bars using `surface-container-highest` at 70% opacity with a 20px backdrop blur. For primary CTAs, apply a subtle linear gradient from `primary` (`#ffb4aa`) to `primary-container` (`#e21b1b`) at a 135-degree angle.

---

## 3. Typography
We utilize a high-contrast pairing that balances futuristic utility with humanistic readability.

- **Display & Headline (Space Grotesk):** This is our "Impact" face. It should be set with tight letter-spacing (-2% to -4%) to feel aggressive and compact. 
    - **Display-LG (3.5rem):** Reserved for hero slogans. Use `on-surface` (`#e21b1b`) or knockout white.
- **Body & Title (Manrope):** A sophisticated sans-serif that ensures professional clarity.
    - **Body-LG (1rem):** Our standard for descriptive text. Ensure a generous line-height (1.6) to provide breathing room against the heavy headlines.
- **Hierarchy Hint:** Headlines should often be all-caps when using `label-md` or `headline-sm` to lean into the "Athletic Editorial" aesthetic.

---

## 4. Elevation & Depth
In "The Kinetic Arena," we do not use shadows to mimic light; we use tonal layering to mimic physical presence.

- **The Layering Principle:** Depth is achieved by stacking. A card (`surface-container-high`) sits on a section (`surface-container-low`) to create natural lift.
- **Ambient Shadows:** Shadows are rarely used. When required for "Floating" buttons, use a 40px blur, 0% spread, and 8% opacity of the `on-background` color. It should feel like a faint glow, not a drop shadow.
- **The "Ghost Border" Fallback:** If a container requires a boundary (e.g., a complex schedule table), use a "Ghost Border" using `outline-variant` (`#5d3f3b`) at 15% opacity. Never use 100% opaque lines.
- **Movement:** Depth is also conveyed through scroll-triggered parallax. Foreground text (Display-LG) should move at a 1.2x speed relative to background imagery to create a sense of three-dimensional space.

---

## 5. Components

### Hero Sections
- **Style:** Full-bleed `surface-container-lowest` backgrounds with a background image at 30% opacity. 
- **Interaction:** Implement a "reveal" animation where the headline (`display-lg`) slides up from a masking container as the user scrolls.

### Buttons
- **Primary:** `primary-container` (`#e21b1b`) background, `on-primary-container` text. 0px radius. Rectangular and bold.
- **Secondary:** Transparent background with a `ghost-border` (`outline-variant` @ 20%). On hover, fill with `on-surface` and invert text.
- **Padding:** 1.5rem horizontal, 0.9rem vertical (`spacing-8` and `spacing-4`).

### Schedule Tables
- **Layout:** Forbid dividers. Use alternating row colors: `surface` and `surface-container-low`.
- **Typography:** Time slots in `label-md` (Space Grotesk, Bold, All-Caps). Class names in `title-md` (Manrope).
- **Active State:** The current day's column should be highlighted with a `primary` top-border of 4px.

### Contact Forms
- **Input Fields:** `surface-container-highest` background. No border, only a 2px bottom-accent that turns `primary` on focus.
- **Error States:** Use `error` (`#ffb4ab`) for helper text. The input background shifts to `error-container` at 10% opacity.

### Cards (Class/Trainer Profiles)
- **Constraint:** 0px border-radius. Use `surface-container-high` for the card body. 
- **Image:** Grayscale by default, transitioning to full color on hover with a 1.05x scale transform.

---

## 6. Do's and Don'ts

### Do:
- **Use "White Space" as a Weapon:** Use `spacing-20` (4.5rem) or `spacing-24` (5.5rem) between sections to create an elite, gallery-like feel.
- **Embrace Asymmetry:** Offset your headlines. Let a Class Schedule overflow the right side of the container while the description stays left-aligned.
- **High Contrast:** Ensure all red-on-black text passes WCAG AA accessibility by using the `primary-fixed` or `primary` tokens.

### Don't:
- **No Rounding:** Never use a border-radius. It softens the brand’s "aggressive" edge. Everything is a hard angle.
- **No Generic Grids:** Avoid the "3-column feature row" whenever possible. Try a 2/3 and 1/3 split to create visual tension.
- **No Solid Lines:** Do not use 1px solid borders to separate content. Use the spacing scale (`spacing-12`+) or background color shifts.
- **No Pure White:** Use `on-surface` (`#e22e2e`) for body text to reduce eye strain against the black background; keep pure white only for high-impact headlines.```