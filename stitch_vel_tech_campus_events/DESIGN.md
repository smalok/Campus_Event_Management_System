```markdown
# Design System Document: The Academic Curator

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"The Academic Curator."** Unlike standard university portals that feel like cluttered bulletin boards, this system treats campus life as a premium editorial experience. It moves away from the rigid, boxy layouts of legacy academic software in favor of an open, airy, and sophisticated environment.

The "Curator" identity is achieved through **intentional asymmetry**, where large display typography creates a rhythmic pace, and overlapping elements break the "grid-lock" to suggest a modern, forward-thinking institution. This isn't just an event management tool; it is a digital window into the prestige and energy of university life.

## 2. Colors & Tonal Depth
The palette is rooted in the university’s heritage but elevated through Material Design 3 logic to ensure depth and accessibility.

### The Color Roles
- **Primary (`#a20513`):** Reserved for high-intent actions. It is the "pulse" of the interface.
- **Secondary (`#4f5e81`):** A sophisticated Navy used for navigation and grounding elements.
- **Surface Tiers:** We utilize a spectrum from `surface_container_lowest` (#ffffff) to `surface_dim` (#d0dbed) to create a sense of physical architecture.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Boundaries must be established through color-blocking. 
- A card should never be "outlined." Instead, place a `surface_container_lowest` card on top of a `surface_container_low` section. 
- Use the shift from `surface` (#f8f9ff) to `surface_container` (#e6eeff) to delineate the transition from a hero area to a content grid.

### Signature Textures & Glassmorphism
To avoid a "flat" feel, use **Glassmorphism** for floating elements such as sticky navigation bars or mobile action sheets. 
- **Application:** Use `surface` colors at 80% opacity with a `20px` backdrop-blur. 
- **Gradients:** For primary CTAs, apply a subtle linear gradient from `primary` (#a20513) to `primary_container` (#c62828) at a 135-degree angle. This adds "soul" and a tactile, pressed-ink quality to the crimson.

## 3. Typography: The Editorial Voice
We use **Inter** not as a utility font, but as an editorial typeface. The hierarchy is designed to guide the eye through high-contrast scales.

- **Display & Headlines:** Use `display-lg` and `headline-lg` for event titles. Tighten the letter-spacing (`-0.02em`) to create a dense, authoritative "news" feel.
- **The Label Strategy:** All `label-md` and `label-sm` elements should be set in **ALL CAPS** with a generous letter-spacing (`+0.05em`). This distinguishes metadata (dates, locations) from body content.
- **Brand Resonance:** The interplay between the massive display type and the clean, functional body text mimics the layout of a high-end academic journal, balancing prestige with readability.

## 4. Elevation & Depth: Tonal Layering
In this design system, depth is a product of light and layering, not structural lines.

### The Layering Principle
Think of the UI as stacked sheets of fine paper. 
- **Level 0 (Base):** `surface` (#f8f9ff)
- **Level 1 (Sections):** `surface_container_low` (#eff4ff)
- **Level 2 (Cards):** `surface_container_lowest` (#ffffff)
This creates a "soft lift" that feels natural and premium.

### Ambient Shadows & Ghost Borders
- **Shadows:** When an element must "float" (e.g., a modal or a primary action button), use an **Ambient Shadow**. 
  - *Values:* `0px 12px 32px rgba(18, 28, 42, 0.06)`. 
  - The shadow is tinted with the `on_surface` color to ensure it looks like a natural occlusion of light rather than a gray smudge.
- **The Ghost Border:** If contrast is required for accessibility (e.g., in forms), use a "Ghost Border" using the `outline_variant` token at **15% opacity**. It should be felt, not seen.

## 5. Components

### Buttons
- **Primary:** `8px` rounded. Uses the Signature Crimson Gradient. High-contrast `on_primary` (#ffffff) text.
- **Secondary:** Transparent background with a `Ghost Border`. Text in `primary`.
- **Tertiary:** No background or border. `label-md` styling. Used for low-emphasis actions like "Cancel" or "View All."

### Cards (The Event Entry)
- **Rules:** `12px` corner radius. No borders. Use `surface_container_lowest` on a `surface_container_low` background.
- **Interaction:** On hover, the card should lift using an **Ambient Shadow** and scale by 1.02%.
- **Content:** Forbid the use of divider lines. Use `16px` or `24px` of vertical white space to separate the event image from the title.

### Input Fields
- **Styling:** `surface_container_lowest` background. 
- **States:** On focus, the `Ghost Border` transitions to a 2px solid `primary` (#a20513) only on the *bottom* edge, mimicking a premium stationery feel.

### Chips (Event Tags)
- **Visuals:** `9999px` (Full) rounded. Use `secondary_container` with `on_secondary_container` text. This provides a soft, tech-forward contrast to the sharp editorial headers.

### Additional Component: The "Live" Indicator
For ongoing events, use a small `8px` pulse dot in `primary` next to a `label-sm` "Happening Now" tag. This adds a layer of dynamic urgency to the static grid.

## 6. Do's and Don'ts

### Do
- **Do** use asymmetrical margins. For example, a page title might be offset further to the right than the body text to create a modern editorial vibe.
- **Do** use large, high-quality imagery that bleeds to the edges of containers.
- **Do** rely on the `surface` color shifts to define the "start" and "end" of content areas.

### Don't
- **Don't** use 100% black text. Always use `on_surface` (#121c2a) for primary text to maintain a softer, premium contrast.
- **Don't** use "Drop Shadows" on every card. If everything floats, nothing is important. Use Tonal Layering first.
- **Don't** use dividers or horizontal rules. If the content feels cluttered, increase the spacing (`gap-8` or `gap-12`) instead of adding a line.
- **Don't** use standard "blue" for links. All interactive triggers must be `primary` (Crimson) or `secondary` (Navy) to stay on-brand.

---
*End of Document. This design system is intended to be a living framework for the Vel Tech Campus Events ecosystem.*```