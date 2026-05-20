## 2025-05-14 - Modal Accessibility and Focus Restoration
**Learning:** Static containers used as modals or lightboxes must include `tabindex="-1"` to allow programmatic focus via JavaScript (`.focus()`). Restoring focus to the previously active element (`document.activeElement`) upon closing the modal is crucial for a seamless keyboard navigation experience.
**Action:** Always save the `lastFocusedElement` before opening an overlay and restore it on close. Use `tabindex="-1"` on modal containers to ensure they can capture focus and intercept keyboard events correctly.
