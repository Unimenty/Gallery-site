# Palette's Journal - Critical Learnings

## 2026-06-18 - [Accessibility & Focus Management in Custom Infinite Grids]
**Learning:** In highly customized, JavaScript-driven UI components like infinite/recycled grids, accessibility is often overlooked. Simply adding `click` listeners is insufficient; elements must be promoted to the accessibility tree using `role="button"` and `tabindex="0"`, and keyboard activation (`Enter`/`Space`) must be manually implemented. Furthermore, programmatic focus management (saving and restoring `document.activeElement`) is essential for maintaining context when navigating in and out of overlays.

**Action:** Always ensure custom interactive elements have semantic roles, keyboard listeners, and participate in a robust focus management system that includes `Escape` key support for closing modals.
