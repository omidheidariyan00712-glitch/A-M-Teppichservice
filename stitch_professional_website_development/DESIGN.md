# Design System Strategy: A&M Teppichservice

## 1. Overview & Creative North Star: "The Artisanal Purist"

The design system is built upon a Creative North Star titled **"The Artisanal Purist."** In an industry often cluttered with loud, "salesy" graphics, this system takes an editorial approach that treats carpet care as a craft rather than a chore. It combines the deep, authoritative blues of the industrial sector with the warm, inviting golds of luxury home maintenance.

This design system breaks away from "standard" service templates through:
*   **Intentional Asymmetry:** Overlapping high-fidelity imagery with content containers to create a sense of physical space.
*   **Tonal Depth:** Replacing harsh outlines with a sophisticated hierarchy of layered surfaces.
*   **Breathing Room:** High-contrast typography scales supported by generous white space to signal premium quality and meticulousness.

---

## 2. Color Philosophy

The palette transitions from the "Deep Blue" of expertise to "Warm Gold" accents that signify value.

### The "No-Line" Rule
**Explicit Instruction:** Use of 1px solid borders for sectioning or card containment is strictly prohibited. Define boundaries solely through background color shifts. For instance, a `surface-container-low` section should sit directly against a `background` canvas.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine materials.
*   **Level 0 (Base):** `background` (#f6fafd)
*   **Level 1 (Sectioning):** `surface-container-low` (#f0f4f7)
*   **Level 2 (Cards/Interaction):** `surface-container-lowest` (#ffffff)
*   **Level 3 (Floating/Contextual):** `surface-bright` (#f6fafd)

### The "Glass & Gradient" Rule
Main CTAs and floating trust indicators should utilize subtle gradients (e.g., `primary` transitioning to `primary-container`) or Glassmorphism. Use semi-transparent surface colors with a `backdrop-blur: 12px` to make elements feel integrated into the environment rather than pinned on top.

---

## 3. Typography

The typography strategy pairs **Plus Jakarta Sans** (Display/Headlines) for a modern, architectural feel with **Manrope** (Body/UI) for superior legibility.

*   **Display (Plus Jakarta Sans):** Large, bold, and authoritative. Used for Hero statements to command attention immediately.
*   **Headline (Plus Jakarta Sans):** Used to introduce service sections. The tight letter-spacing and heavy weight provide an "editorial" feel.
*   **Body (Manrope):** Set with generous line-height (1.6) to ensure the technical details of the cleaning process remain approachable.
*   **Label (Manrope):** Used for "Overlines" (all caps, wide tracking) above headlines to provide context, such as "ERGEBNISSE" or "UNSERE LEISTUNGEN."

---

## 4. Elevation & Depth

Hierarchy is achieved through **Tonal Layering** rather than structural lines.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a soft, natural lift that mimics paper on a desk.
*   **Ambient Shadows:** For floating elements like the "Kostenloses Angebot" CTA, use a shadow with a 24px blur, 4% opacity, using a tinted version of `on-surface` (#171c1f). This mimics natural ambient light.
*   **The "Ghost Border" Fallback:** If a boundary is strictly required for accessibility, use the `outline-variant` token at **15% opacity**. Never use 100% opaque borders.
*   **Textural Glass:** Use backdrop blurs on contact form containers to allow the high-resolution carpet textures in the background to bleed through, softening the visual weight.

---

## 5. Components

### Hero Sections
*   **Layout:** Use a split-screen or 60/40 asymmetrical layout. 
*   **Visuals:** Overlap the `surface-container-lowest` content card slightly over the hero image to create depth.
*   **Signature:** Incorporate the "Warm Gold" (`secondary`) for secondary CTA text or icon accents to guide the eye.

### Service Cards
*   **Structure:** No dividers. Use `title-md` for the service name and `body-sm` for descriptions.
*   **Interaction:** On hover, shift the background from `surface-container-lowest` to `surface-bright` and increase the ambient shadow slightly.

### Trust Indicators (Ratings & Stats)
*   **Stats:** Large `display-sm` numbers in `primary`.
*   **Star Ratings:** Use `secondary` (Gold) for stars. Group them in a floating "Glass" container (`surface` at 80% opacity + blur) placed over high-quality "Before/After" imagery.

### Contact Forms
*   **Inputs:** Use `surface-container-highest` for input backgrounds with no border. 
*   **Active State:** On focus, transition the background to `surface-container-lowest` and add a "Ghost Border" using the `primary` color at 20% opacity.

### Buttons
*   **Primary:** `primary` background, `on-primary` text. Use `DEFAULT` (0.5rem) roundedness for a modern but professional feel.
*   **Secondary:** `surface-container-highest` background. Subtle, non-intrusive.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical image placement to break the "grid" feel.
*   **Do** use the `secondary` gold color sparingly as a "highlight" for high-value information (ratings, contact numbers).
*   **Do** prioritize vertical whitespace over lines or dividers to separate content.

### Don't
*   **Don't** use pure black (#000000) for text; use `on-surface` (#171c1f) to maintain the slate-gray tonal harmony.
*   **Don't** use standard "drop shadows" with high opacity. They look dated and cheap.
*   **Don't** use sharp 0px corners. Stick to the `DEFAULT` (8px) or `lg` (16px) scales to maintain a "trustworthy and approachable" persona.