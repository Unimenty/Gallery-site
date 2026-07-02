## 2026-07-02 - [Accessibility in Luxury Cursor-less UIs]
**Learning:** High-fashion/luxury UIs often hide the default cursor (`cursor: none`) to enhance aesthetics, which creates a critical accessibility barrier for keyboard users.
**Action:** Always implement high-contrast `:focus-visible` outlines and rigorous programmatic focus management (using `tabindex="-1"` on modal containers and restoring focus to a `lastFocusedElement`) to ensure the site remains navigable without a mouse.
>>>>>>> REPLACE