# Design System Document

## 1. Overview & Creative North Star: "The Curated Canvas"

This design system is a modern dialogue between the mathematical precision of Neoplasticism and the breathing room of high-end editorial design. It moves beyond a mere replication of Piet Mondrian’s work, instead treating the digital interface as **"The Curated Canvas."**

The objective is to balance the bold, structural authority of the 20th-century avant-garde with a refined, 21st-century educational atmosphere. We achieve this through:
*   **Intentional Asymmetry:** Rejecting centered, "safe" layouts for dynamic, 12-column geometric compositions.
*   **Structural Anchors:** Using thick black lines not just as borders, but as architectural elements that frame content and guide the eye.
*   **High-Contrast Tension:** Pitting the classic, authoritative weight of Playfair Display against the functional clarity of Inter.

This is not a template; it is a composition. Every block of color and every line must feel like a deliberate choice.

---

## 2. Colors & Surface Logic

The palette uses a primary triad (Blue, Red, Yellow) set against a sophisticated, warm neutral base. The goal is vibrancy without chaos.

### Tonal Foundation
*   **Background (Off-White):** `#F9F8F4` — The primary canvas.
*   **Surface (Light Gray):** `#E8E6DF` — For secondary sections and subtle shifts.
*   **Structural Black:** `#111111` — Used for all typography and structural framing.

### The Primary Triad (Strategic Use)
*   **Primary Blue (`#1A3A8F`):** Institutional strength. Use for primary actions and navigation.
*   **Secondary Red (`#D62828`):** Emotional energy. Use for accents, markers, or urgent notifications.
*   **Tertiary Yellow (`#F7C948`):** Creativity and light. Use exclusively for special Call-to-Actions (CTAs) and "moments of joy."

### The "No-Line" Rule vs. The "Structural" Rule
To maintain an editorial feel:
1.  **Prohibit 1px Borders:** Never use thin grey dividers. They feel generic.
2.  **Boundary Definition:** Transition between sections using background color shifts (e.g., moving from `surface` to `surface_container_low`).
3.  **Signature Framing:** Only use the `Structural Black` lines (3-4px) when a section requires a hard, conceptual frame or a "Mondrian-style" block separation.

---

## 3. Typography: Editorial Authority

The typographic hierarchy is designed to feel like a premium art publication.

*   **Titles & Headlines (Playfair Display):**
    *   **Style:** Bold (700-900), tight tracking (-0.02em to -0.05em).
    *   **Role:** Conveys tradition and "The Institution." Large display sizes should be used with ample white space to create an "Editorial Hero" effect.
*   **Body & UI (Inter):**
    *   **Style:** Regular (400) for long-form; SemiBold (600) for labels.
    *   **Role:** Provides a clean, modern contrast to the serif headings. It ensures high readability for educational content.

---

## 4. Elevation & Depth: Tonal Layering

Traditional shadows and 3D effects are strictly forbidden. We create depth through **Layering** and **Tension**.

*   **The Layering Principle:** Use the `surface-container` tiers to stack elements. A card (`surface_container_lowest`) sitting on a section (`surface_container_low`) creates a "paper-on-paper" lift that is sophisticated and flat.
*   **Glassmorphism for Floating Elements:** To add "digital soul," use backdrop blurs on navigation bars or modals. Use a semi-transparent version of `#F9F8F4` with a `12px` to `20px` blur. This softens the hard geometric lines of the system.
*   **Ambient Shadows:** If a floating action button or modal *must* have a shadow, it must be invisible. Use the `on_surface` color at 4% opacity with a blur radius of 32px or higher. It should feel like "weight" rather than a "shadow."

---

## 5. Components: The Geometric Primitive

All components adhere to a strict **0px to 4px border-radius**. Sharp corners are the default.

### Buttons
*   **Primary:** Background: Primary Blue (`#1A3A8F`); Text: White; Border: 2px `Structural Black`. No radius.
*   **Secondary:** Background: Transparent; Text: `Structural Black`; Border: 2px `Structural Black`.
*   **Special CTA:** Background: Primary Yellow (`#F7C948`); Text: `Structural Black`; No Border. This is the "high-light" button.

### Cards & Lists
*   **Rule:** Forbid the use of divider lines. 
*   **Implementation:** Separate list items using the spacing scale (e.g., `spacing-4` or `spacing-6`) and subtle background color alternating (Zebra striping using `surface` and `surface_container_low`).
*   **Frames:** When grouping related cards, use a single 3px black line to "anchor" the group to the left side of the grid.

### Input Fields
*   **Styling:** 2px black bottom border only. Labels in `label-md` (Inter SemiBold). No background fill unless the field is in an error state (`error_container`).

### Special Component: "The Mondrian Block"
*   A decorative UI element used to break up long scrolling pages. It is an asymmetrical grid of color blocks (Blue/Yellow/Red) that doubles as a container for quick-link icons or featured stats.

---

## 6. Do's and Don'ts

### Do
*   **Do use asymmetrical whitespace.** Let a headline sit in the top-left of a grid while the body text starts three columns in.
*   **Do use the 3px black line as a structural guide.** It should look like it's holding the page together.
*   **Do treat typography as art.** Mix `display-lg` with `body-sm` for high-contrast, editorial layouts.

### Don't
*   **Don't use all three primary colors in equal proportions.** Choose one "hero" color for the page and use the others as tiny, intentional accents.
*   **Don't use 1px grey borders.** They dilute the strength of the system.
*   **Don't use standard drop shadows.** If it looks like it's "hovering" via a dark shadow, it's wrong. Depth comes from color and stacking.
*   **Don't round your corners.** Stay at 0px wherever possible to maintain the Neoplasticist architectural feel.