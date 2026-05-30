## 2025-05-14 - Modal Accessibility
**Learning:** Static containers used as modals or lightboxes must include `tabindex="-1"` to allow programmatic focus via JavaScript (`.focus()`), ensuring keyboard interaction is successfully captured when the overlay opens.
**Action:** Always add `tabindex="-1"` to overlay containers and call `.focus()` upon opening.

## 2025-05-14 - Focus Restoration Pattern
**Learning:** Save `document.activeElement` to `lastFocusedElement` before opening overlays. Upon closing, restore focus to the saved element. If the saved element is inside a closed menu (like `navOverlay`), redirect focus to the trigger (e.g., `burgerBtn`) to avoid focusing hidden elements.
**Action:** Implement a `restoreFocus()` helper that handles these edge cases.

## 2025-05-14 - Keyboard Support for Custom Grid Items
**Learning:** To enable keyboard accessibility on custom grid items concisely, assign `tabindex="0"` and `role="button"`, then use `el.addEventListener('keydown', e => (e.key === 'Enter' || e.key === ' ') && (e.preventDefault(), el.click()))` to support both activation keys while suppressing scroll.
**Action:** Apply this pattern to all interactive non-button elements.
