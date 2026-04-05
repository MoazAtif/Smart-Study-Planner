```markdown
# Design System Document: The Scholarly Horizon

## 1. Overview & Creative North Star: "The Intellectual Sanctuary"
This design system moves away from the frantic, high-intensity "productivity hack" aesthetic. Instead, we are building an **Intellectual Sanctuary**. The objective is to facilitate deep work through a "Productive & Calm" environment that feels less like a utility and more like a high-end editorial journal.

**Creative North Star: The Curated Workspace**
We break the "template" look by utilizing intentional asymmetry—placing larger, airy headers against compact, dense data modules. We avoid the rigid, boxed-in feel of standard SaaS by using **Tonal Layering** and **Editorial Spacing**. Elements should feel like they are resting on a physical desk, organized by a thoughtful curator.

---

## 2. Colors & Surface Philosophy
The palette is rooted in a deep, scholarly Indigo (`primary`), balanced by the airiness of Slate (`secondary`) and the "flow state" energy of Teal (`tertiary`).

### The "No-Line" Rule
**Borders are a design failure in this system.** To maintain a premium, calm atmosphere, 1px solid borders for sectioning are strictly prohibited. Boundaries must be defined solely through:
- **Background Shifts:** Placing a `surface_container_low` section against a `surface` background.
- **Tonal Transitions:** Using subtle shifts in the surface tier to imply containment.

### Surface Hierarchy & Nesting
Treat the UI as a series of nested layers.
*   **Base Layer:** `surface` (#f7f9fb) — The primary canvas.
*   **Secondary Content:** `surface_container_low` (#f2f4f6) — For sidebars or secondary navigation.
*   **Interactive Cards:** `surface_container_lowest` (#ffffff) — The highest "lift" for focus areas like active study tasks.
*   **Inset Modules:** `surface_container_high` (#e6e8ea) — Use this for "well" styles, such as a calendar grid sitting "inside" a dashboard page.

### The "Glass & Gradient" Rule
For floating elements (modals, dropdowns, or active study timers), use **Glassmorphism**:
*   **Color:** `surface_container_lowest` at 85% opacity.
*   **Effect:** `backdrop-filter: blur(12px)`.
*   **Signature Gradient:** Apply a subtle linear gradient to main CTAs (e.g., `primary` to `primary_container`) to provide "soul" and depth that flat hex codes lack.

---

## 3. Typography: The Editorial Edge
We use a dual-font strategy to balance authority with readability.

*   **Display & Headlines (Manrope):** Chosen for its geometric modernism. High-contrast sizing (e.g., `display-lg` at 3.5rem) should be used to create clear entry points for the eye, breaking the monotony of data-heavy study schedules.
*   **Body & UI (Inter):** The workhorse. It provides maximum legibility for long-form notes and complex schedules.

**Hierarchy as Identity:**
Use `label-md` in all-caps with increased letter-spacing (0.05em) for category headers (e.g., "UPCOMING EXAMS"). This creates a professional, "published" look that distinguishes metadata from content.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often cluttered. This system uses light to imply importance.

*   **The Layering Principle:** Instead of a shadow, place a `surface_container_lowest` card on a `surface_container_low` background. The slight shift in brightness provides a "soft lift."
*   **Ambient Shadows:** For floating action buttons or active task cards, use a tinted shadow: `box-shadow: 0 12px 32px -4px rgba(20, 33, 117, 0.08)`. This uses the `primary` indigo color to make the shadow feel like natural ambient light.
*   **The "Ghost Border" Fallback:** If a divider is mandatory for accessibility, use `outline_variant` (#c6c5d3) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Cards (Subject & Task)
*   **Style:** No borders. Use `surface_container_lowest` for the background.
*   **Spacing:** `xl` (1.5rem) internal padding. 
*   **Detail:** Subject cards should feature a 4px vertical accent line on the left using the `tertiary_fixed` color to denote "Focus Mode."

### Progress Bars
*   **Track:** `surface_container_highest`.
*   **Indicator:** A gradient from `tertiary` to `tertiary_fixed`. 
*   **Shape:** `full` roundedness. Avoid segmented bars; use smooth, continuous motion to reflect "flow."

### Calendar-Style Schedule
*   **Grid:** Forbidden. Use whitespace to define days. 
*   **Current Day:** Highlight with a `secondary_container` background and a `display-sm` date numeral.
*   **Events:** Use `glassmorphism` for overlapping study sessions to show "density" without visual noise.

### Buttons
*   **Primary:** `primary` background with `on_primary` text. `md` (0.75rem) corner radius.
*   **Secondary:** `secondary_container` background. No border.
*   **State:** On hover, shift background to `primary_container`—never use a "darker" version of the base color; use the system's container tokens.

### Input Fields
*   **Structure:** Minimalist. `surface_container_low` background with a bottom-only "focus line" using `primary`.
*   **Labels:** Always use `label-md` positioned above the field, never as placeholder text.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Negative Space:** If a section feels crowded, increase the margin rather than adding a divider.
*   **Use Tonal Priority:** The most important task should be the brightest element on the screen (`surface_container_lowest`).
*   **Animate Transitions:** Use "Slow-In, Fast-Out" easing for container expansions to mimic a calm, deliberate movement.

### Don't:
*   **Don't use pure black:** Always use `on_surface` (#191c1e) for text to maintain the "calm" atmosphere.
*   **Don't use hard corners:** Every element must have at least a `sm` (0.25rem) radius to avoid a "sharp" or aggressive feel.
*   **Don't over-accent:** Limit the `tertiary` (Teal) to progress and action—overuse breaks the "Calm" promise.

---

## 7. Contextual Component: The "Focus Shroud"
A unique component for this system: when a user enters "Deep Study Mode," all background `surface` elements dim to `inverse_surface`, while the active task card retains its `surface_container_lowest` brilliance, physically pulling the user's attention into the "Light" of their work.```