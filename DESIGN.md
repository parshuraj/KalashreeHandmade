# Design System: Modern Heritage

## 1. Creative North Star: "The Curated Heirloom"
This design system is built on the philosophy of **The Curated Heirloom**. We are not building a standard e-commerce shop; we are designing a digital gallery that honors the tension between ancestral craftsmanship and modern minimalism. 

To achieve this, the UI must move away from "boxed-in" web patterns. We embrace **Intentional Asymmetry**—where product imagery may bleed off the edge of a container—and **Editorial Breathing Room**, utilizing expansive white space to elevate each piece of jewelry as a singular work of art. The interface should feel like a high-end physical lookbook: tactile, layered, and quiet.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule
The palette is rooted in the earth and the forge. We use deep emerald to provide a sense of grounded history and gold to highlight the artisanal spark.

### Palette Application
- **Primary & Containers:** `primary` (#003527) and `primary_container` (#064e3b) are reserved for moments of high impact—hero section backgrounds, footer foundations, and primary action states.
- **The Accents:** `secondary` (#735c00) and `secondary_fixed` (#ffe088) represent the "rich gold" requested. Use these sparingly for interactive elements or status indicators to maintain their premium feel.
- **The Neutrals:** `surface` (#faf9f8) and `surface_container_lowest` (#ffffff) provide the "airy white space" that allows the jewelry photography to breathe.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning content. Boundaries are defined exclusively through:
1.  **Background Shifts:** Transitioning from `surface` to `surface_container_low`.
2.  **Vertical Space:** Utilizing the larger increments of our spacing scale (e.g., `spacing.16` or `spacing.20`) to denote new sections.

### Glass & Gradient Implementation
Main CTAs and primary navigation overlays should utilize **Glassmorphism**. Apply `surface_container` colors at 80% opacity with a `backdrop-blur` of 12px. For high-end backgrounds, use a subtle linear gradient from `primary` (#003527) to `primary_container` (#064e3b) at a 135-degree angle to simulate the depth of a polished emerald stone.

---

## 3. Typography: The Editorial Voice
Our typography is a conversation between the old world and the new.

- **Display & Headlines (Noto Serif):** These are our "Heritage" anchors. Use `display-lg` and `headline-lg` for product titles and collection names. Ensure tracking (letter-spacing) is set slightly tighter (-2%) for a more customized, high-fashion appearance.
- **Body & Titles (Manrope):** The modern counterpart. `body-lg` and `body-md` provide a clean, legible contrast to the ornate serif.
- **Technical Labels (Space Grotesk):** We use a monospaced feel for SKU numbers, dimensions, and material specs. This provides an "Artisan’s Ledger" feel, signaling precision and authenticity.

---

## 4. Elevation & Depth: Tonal Layering
We reject the heavy shadows of the early web. In this design system, depth is a whisper, not a shout.

- **The Layering Principle:** Use the `surface-container` tiers to stack elements. A product detail card (`surface_container_lowest`) should sit atop a `surface_container_low` gallery section. This creates a "Paper-on-Paper" effect.
- **Ambient Shadows:** For floating elements (like a mini-cart or high-level modal), use a shadow with a blur of 40px and 4% opacity, using the `on_surface` color as the shadow tint.
- **The "Ghost Border":** If a separation is required for accessibility, use the `outline_variant` token at **15% opacity**. This creates a suggestion of a boundary without cluttering the visual field.

---

## 5. Components: The Artisanal Toolkit

### Buttons
- **Primary:** `primary` background with `on_primary` text. Shape: `rounded-sm` (0.125rem) to maintain a sharp, sophisticated edge.
- **Secondary (The Gold):** Use an `outline` button with a `secondary` (#735c00) text and a `secondary` Ghost Border.
- **Tertiary:** Pure text-link using `label-md` (Space Grotesk) in all caps with 1.5pt letter spacing.

### Product Cards
- **Construction:** No borders. Use a `surface_container_lowest` background. 
- **Spacing:** Use `spacing.4` for internal padding.
- **Interaction:** On hover, the image should subtly scale (1.02x) while the background shifts to `surface_container_high`. Avoid drop shadows on hover; focus on the tonal shift.

### Inputs & Selectors
- **Fields:** Floating labels using `manrope`. Use a bottom-border only (the "Editorial Input") using `outline_variant` at 40% opacity. 
- **Checkboxes/Radios:** Use the `secondary` (Gold) color for the "checked" state to signify a premium selection.

### Curated Component: The "Provenance" List
A custom list style for jewelry specifications (Carat, Clarity, Metal).
- **Style:** No dividers. Use `spacing.3` between items. 
- **Typography:** The attribute (e.g., "METAL") is in `label-sm` (Space Grotesk), and the value (e.g., "18K Gold") is in `body-md` (Manrope).

---

## 6. Do’s and Don’ts

### Do
- **Do** use asymmetric layouts. Place a hero image off-center and balance it with a `display-lg` headline.
- **Do** leverage the full `spacing.24` (8.5rem) for section gaps to maintain the "Airy" requirement.
- **Do** use high-resolution, "lifestyle" photography where the jewelry is shown in natural, soft lighting.

### Don’t
- **Don’t** use the `error` red for anything other than critical form failures. Even then, keep the icon small and sophisticated.
- **Don’t** use rounded corners larger than `rounded-md` (0.375rem). This brand is about precision and structure; overly round shapes feel too "tech" or "playful."
- **Don’t** use "Sale" badges in bright colors. Use a `surface_container_highest` chip with `secondary` (Gold) text for a quiet luxury approach to promotions.