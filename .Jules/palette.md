# Palette's Journal - High-Fashion Photography Portfolio

## 2025-05-14 - Keyboard Accessibility in "Luxury" Designs
**Learning:** High-fashion "luxury" websites often use `cursor: none` or custom cursors to create a specific aesthetic, which inadvertently hides focus indicators for keyboard users. Relying on default browser focus states is insufficient in these environments. Additionally, virtualized grids require dynamic synchronization of ARIA labels to prevent stale screen reader announcements.
**Action:** Always implement high-contrast `:focus-visible` outlines with a negative `outline-offset` for gallery items and a positive offset for buttons to ensure visibility. For infinite grids, update ARIA attributes inside the `render()` loop alongside visual updates.
