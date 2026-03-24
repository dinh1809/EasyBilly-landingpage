# Design System Document

## 1. Overview & Creative North Star: "The Verdant Editor"

This design system moves away from the rigid, gamified "blocks" common in language apps, opting instead for a **High-End Editorial** experience. We treat language learning not as a chore of memorization, but as an immersive exploration of culture and nuance.

**The Creative North Star: "The Verdant Editor"**
The system mimics a premium boutique magazine—airy, sophisticated, yet pulsing with organic life. We use "The Verdant Editor" to guide our decisions: layouts should feel curated and spacious, using bold typography to anchor the eye, while the "mischievous" personality is injected through subtle asymmetry and gold accents that break the expected grid.

### Breaking the Template
*   **Intentional Asymmetry:** Avoid perfect centering. Offset images or text blocks slightly (using the `spacing-3` or `spacing-4` tokens) to create a sense of movement.
*   **Overlapping Surfaces:** Allow cards to slightly overlap hero sections or each other to create a tactile, paper-like depth.
*   **Scale Contrast:** Use extreme variance between `display-lg` headings and `body-md` text to create an authoritative, editorial hierarchy.

---

## 2. Colors & Surface Soul

The palette is rooted in deep botanical greens and ethereal mints, punctuated by a "Golden Insight" accent.

### The "No-Line" Rule
**Strict Mandate:** 1px solid borders for sectioning are prohibited. 
Separation must be achieved through:
1.  **Background Shifts:** Placing a `surface-container-low` card on a `background` (Soft Mint #E6FFF5).
2.  **Tonal Transitions:** Using a soft gradient to define the end of a header and the start of a scrollable area.

### Surface Hierarchy & Nesting
Treat the UI as a series of nested, organic layers. 
*   **Base Layer:** `background` (#E6FFF5) – The canvas.
*   **Secondary Layer:** `surface-container` (#DBF3EA) – For grouping related lesson modules.
*   **Top Layer:** `surface-container-lowest` (#FFFFFF) – High-contrast cards that "pop" against the mint background.

### The "Glass & Gradient" Rule
To achieve a premium feel, use **Glassmorphism** for floating navigation bars or vocabulary overlays.
*   **Token:** `surface-variant` at 60% opacity with a `20px` backdrop-blur.
*   **Signature Gradient:** For primary CTAs and Progress tracks, use a linear gradient: `primary` (#00522E) to `primary-container` (#006D3F) at a 135-degree angle. This adds "soul" and dimension that flat hex codes lack.

---

## 3. Typography: Editorial Authority

We use **Be Vietnam Pro** (a sophisticated alternative to Nunito with better Vietnamese diacritic support) for expression and **Inter** for functional clarity.

*   **Display & Headlines (Be Vietnam Pro):** These are your "hooks." Use `display-lg` for unit titles. The bold weight paired with the soft colors creates a "Friendly but Authoritative" tone.
*   **Body & Labels (Inter):** These are for high-readability. Inter’s tall x-height ensures that complex Vietnamese tone marks (like in *nguyễn*) remain legible even at `body-sm`.
*   **Editorial Spacing:** Always increase line-height for body text to `1.6` to maintain the "Airy" feel requested.

---

## 4. Elevation & Depth: Tonal Layering

We do not use shadows to indicate "shadows"; we use them to indicate "atmosphere."

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-lowest` card on a `surface-dim` background. This creates a soft, natural lift.
*   **Ambient Shadows:** For floating elements (like a "Billy" mascot tip), use a "Botanical Shadow": 
    *   `Color: on-surface` (#091F1A) at 6% opacity.
    *   `Blur: 40px`, `Y-Offset: 12px`.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke (e.g., in high-contrast mode), use `outline-variant` (#BEC9BE) at **15% opacity**. Never use 100% opacity.

---

## 5. Components & Interaction

### Cards (The Core Pattern)
*   **Radius:** Use `xl` (3rem/48px) for main containers and `lg` (2rem/32px) for internal cards.
*   **Layout:** No dividers. Use `spacing-6` (2rem) of vertical white space to separate content chunks within a card.

### Buttons (The "Billy" Bounce)
*   **Primary:** `primary` background with `on-primary` text. `xl` roundedness.
*   **Secondary:** `secondary-container` background. These should feel "softer" and more approachable.
*   **Mischievous Gold Accent:** Use the `tertiary_fixed` (#FFDF9C) gold for "Eureka" moments or streaks. It should be used sparingly (less than 5% of the screen) to maintain its premium status.

### Progress & Input
*   **Language Inputs:** Text inputs should have no bottom border. Use a `surface-container-highest` background with `xl` rounding.
*   **Elegant Gradients:** Progress bars should use the `primary` to `primary-container` gradient, appearing to "grow" like a vine across the top of the screen.

### Unique Component: "The Insight Overlay"
A semi-transparent glass sheet (`surface` at 80% with blur) that slides up asymmetrically (tilted 1-2 degrees) to provide "mischievous" linguistic tips or cultural secrets.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical margins. A lesson card might have a `spacing-8` left margin and a `spacing-4` right margin to feel "editorial."
*   **Do** embrace white space. If you think there is enough space, add `spacing-2` more.
*   **Do** prioritize Vietnamese typography. Ensure tone marks never collide with the line above.

### Don’t
*   **Don’t** use a divider line. If you feel the need for one, use a background color shift instead.
*   **Don’t** use pure black (#000000). Always use `on-surface` (#091F1A) for text to maintain the soft, organic palette.
*   **Don’t** use sharp corners. Everything—from checkboxes to full-screen modals—must use at least the `md` (1.5rem) corner radius.