## 2025-05-14 - Accessible Luxury & Custom Cursors
**Learning:** In high-fashion/photography portfolios that use `cursor: none` for a minimalist aesthetic, standard visual cues are lost. Keyboard users are completely blind without high-contrast focus indicators. Additionally, in dynamic "Platinum Grid" engines that recycle DOM elements, accessibility metadata (labels, roles) must be explicitly managed within the render loop to prevent stale or missing announcements.

**Action:** Always implement high-contrast `:focus-visible` outlines when system cursors are hidden. Ensure the grid's item creation logic injects `tabindex="0"`, `role="button"`, and dynamic `aria-label` based on current item metadata to maintain a predictable accessibility tree during infinite scrolling.
