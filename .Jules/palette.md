# Palette's UX Journal

## 2026-06-22 - Infinite Grid Accessibility
**Learning:** In virtualized or infinite grids that recycle DOM elements, accessibility metadata (like `aria-label`) must be updated within the recycling loop to ensure screen readers don't announce stale or incorrect information.
**Action:** Always hook into the grid's "update" or "render" function to synchronize ARIA attributes alongside visual properties like `src`.

## 2026-06-22 - Keyboard Navigation with Custom Cursors
**Learning:** Projects that use `cursor: none` or custom magnetic cursors for aesthetic reasons can completely isolate keyboard users if high-contrast `:focus-visible` styles are not implemented.
**Action:** Use a high-contrast `outline` for `:focus-visible` on all interactive elements. For grid items, use a negative `outline-offset` to keep the indicator within the bounds of the element.
