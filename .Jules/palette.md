## 2025-05-15 - Overlay Accessibility & Focus Management
**Learning:** For a luxurious, cursor-less interface, keyboard accessibility is a critical fallback. Overlays (Modals, Nav Menus) must have `tabindex="-1"` for programmatic focus, and use `visibility: hidden` to be correctly removed from the accessibility tree while preserving CSS transitions.
**Action:** Always implement a focus restoration pattern using a `lastFocusedElement` variable to return the user to their previous context when an overlay closes.

## 2025-05-15 - Virtualized Grid Accessibility
**Learning:** In high-performance, infinite grids that recycle or cull DOM elements based on scroll, accessibility metadata (ARIA labels, alt text) must be synchronized within the render/recycle loop to avoid stale information being announced by screen readers.
**Action:** Use `role="button"` and `tabindex="0"` on grid items, and ensure `keydown` listeners (Enter/Space) are attached for activation.
