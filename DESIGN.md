```markdown
# Design System: High-End Editorial Tech Portfolio

## 1. Overview & Creative North Star: "The Kinetic Curator"
This design system is built to dismantle the "standard developer portfolio" trope. Our Creative North Star is **The Kinetic Curator**: a visual language that feels like a high-end fashion editorial met a brutalist coding terminal. 

We move beyond the rigid, centered grid. Instead, we utilize **Intentional Asymmetry** and **Tonal Depth** to create a high-energy, dramatic atmosphere. By leveraging extreme typographic scale—pairing ultra-bold display faces with airy, light-weight body text—we establish an immediate sense of technical authority and creative sophistication. This is not a template; it is a signature digital experience.

---

## 2. Colors & Surface Philosophy
The palette is built on high-contrast shifts between "Void Black" and "Warm Cream," punctuated by a "Neon Lime" kinetic energy.

### Color Strategy
- **Primary (#b6fd55):** Reserved for high-action triggers and "boxed" emphasis. Use this sparingly to maintain its "neon" impact.
- **Surface (#0e0e0e):** The deep-space foundation.
- **Secondary (#e3e3de):** The off-white/cream used for large alternating sections to reset the user's visual palette.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Layout boundaries must be achieved through:
1. **Background Color Shifts:** Transitioning from `surface` to `secondary` (Cream) for a hard editorial break.
2. **Tonal Layering:** Using `surface-container-low` against a `surface` background to define a card or container.

### Surface Hierarchy & Glassmorphism
To create "soul" in the dark theme, utilize the surface-container tiers:
- **Depth Stacking:** Place a `surface-container-highest` element over a `surface` background to create a "lifted" interactive card.
- **The Glass Rule:** For floating geometric shapes or navigation overlays, use a semi-transparent `surface-variant` with a `backdrop-filter: blur(20px)`. This prevents the UI from feeling "pasted on" and allows the background grain texture to bleed through.

---

## 3. Typography: The Editorial Voice
Typography is our primary tool for drama. We pair the industrial weight of **Space Grotesk** with the humanist clarity of **Manrope**.

- **Display & Headlines (Space Grotesk):** Must be set with tight letter-spacing (-0.04em) and ultra-bold weights. This is the "loud" voice of the developer.
- **Body Text (Manrope):** Set in light or regular weights with generous leading (1.6) to provide a sophisticated, breathable counterpoint to the heavy headlines.
- **Boxed Emphasis:** Use the `primary` (#b6fd55) background behind `on-primary` (#3b5f00) text for specific words within headlines to create an "archival tag" aesthetic.

---

## 4. Elevation & Depth
In this system, elevation is a product of light and atmosphere, not structural shadows.

- **The Layering Principle:** Avoid the `z-axis` shadow whenever possible. Instead, use a "Surface Step." A container should be one step higher in the `surface-container` scale than its parent to indicate importance.
- **Ambient Shadows:** If a floating element (like a CTA button) requires a shadow, use a diffuse, 8% opacity shadow tinted with the `primary` hue.
- **The Ghost Border:** For accessibility on interactive inputs, use a "Ghost Border"—the `outline-variant` token at 15% opacity. Never use 100% opaque lines.
- **Signature Texture:** Apply a global SVG noise grain (5% opacity) over the entire UI to kill the "flatness" of digital HEX codes and provide a premium, tactile feel.

---

## 5. Components

### Buttons: The Kinetic Trigger
- **Primary:** Neon Lime (`primary`) fill, pill-shaped (`rounded-full`). Text is `on-primary`.
- **The "Arrow-in-Circle":** All primary buttons must feature a trailing "→" icon enclosed in a circle. On hover, the circle should slide 4px to the right.
- **Tertiary:** No background, just a `label-md` weight text with the "Arrow-in-Circle" icon.

### Pill Labels (Section Headers)
- **Style:** Small, pill-shaped borders using the "Ghost Border" rule. 
- **Content:** Always prefixed with a directional arrow (e.g., `↓ Why Choose Me`). This acts as a wayfinding tool in an asymmetric layout.

### Boxed Headline Words
- **Usage:** Wrap key technical terms in a solid `primary` block.
- **Padding:** `0.2em 0.4em`. This mimics a highlighter or a physical label-maker tag.

### Cards & Projects
- **Rule:** Forbid divider lines.
- **Separation:** Separate project cards using the `Spacing Scale 16` (5.5rem). Use `surface-container-low` for the card body to create a subtle "inner-glow" against the `surface` background.

### Input Fields
- **Style:** Minimalist. No bottom border. Use a `surface-container-high` background with `rounded-md`.
- **Focus State:** A subtle 1px "Ghost Border" at 20% opacity using the `primary` color.

---

## 6. Do's and Don'ts

### Do
- **Embrace the Void:** Use the `24` (8.5rem) spacing token between major sections to let the typography breathe.
- **Overlap Elements:** Let a geometric shape or a high-resolution project image overlap two different surface colors to "stitch" the editorial layout together.
- **Use Micro-Gradients:** Use a subtle gradient from `primary` to `primary-container` on large CTA buttons to give them a "3D Neon" glow.

### Don't
- **Don't Center Everything:** Avoid centered text blocks. Use an asymmetric 12-column grid where the headline starts on Column 2 and the body text starts on Column 6.
- **Don't Use Pure Black Shadows:** Shadows should always be a tinted transparent version of the background.
- **Don't Use Standard Borders:** If you feel the need to draw a line, use a `surface-container` shift instead. 

### Accessibility Note
While the design is "bold," ensure that all `on-primary` text against the `primary` (Neon Lime) background maintains a 4.5:1 contrast ratio. If necessary, use `on-primary-container` for small-scale text.```