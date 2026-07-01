## 2025-05-14 - Keyboard Accessibility in "Cursor-less" Interfaces
**Learning:** Custom hidden cursors (`cursor: none`) used for luxury aesthetics completely break the primary visual feedback loop for interactive elements. In such environments, `:focus-visible` states are not just a best practice but a mandatory functional requirement. High-contrast outlines (2px solid #fff) with internal offsets for grid items ensure that keyboard users can navigate complex, dynamic layouts without a mouse.
**Action:** Always pair `cursor: none` with high-contrast `:focus-visible` styles and programmatic focus management (tabindex="-1" on modals, .focus() on open/close) to ensure the interface remain accessible and intuitive.

## 2025-05-14 - Accessibility in Recycled Grid Systems
**Learning:** In infinite or virtualized grids where DOM elements are recycled (e.g., Platinum Grid Engine), accessibility metadata like `aria-label` and `alt` text must be updated within the render/recycle loop alongside visual properties like `src`. Simply setting these attributes on initial creation leads to stale or incorrect context for screen reader users as they scroll through the virtual space.
**Action:** Ensure all accessibility attributes are synchronized in the grid's update/recycling logic to maintain an accurate mental model for non-visual users.
