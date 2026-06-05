# Palette's Journal - Critical UX/Accessibility Learnings

## 2024-05-24 - Focus Management in Editorial Portfolio Grids
**Learning:** Static containers used as modals or lightboxes (like `#lightbox` or `#services`) must include `tabindex="-1"` to allow programmatic focus via JavaScript (`.focus()`). This ensures that keyboard interaction is successfully captured as soon as the overlay opens, preventing focus from being "lost" in the background.

**Action:** Always add `tabindex="-1"` to overlay containers and call `.focus()` immediately after changing their display state to 'flex' or 'block'.

## 2024-05-24 - Keyboard Support for Infinite Grid Engines
**Learning:** In highly customized JS-driven gallery engines (like the "Platinum Grid Engine"), gallery items must be explicitly marked as interactive using `tabindex="0"` and `role="button"` to be reachable via Tab. Furthermore, since these items often lack a semantic `<a>` or `<button>` wrapper, explicit "Enter" and "Space" key listeners must be added to trigger the same action as a click.

**Action:** When implementing custom grid items, use `el.setAttribute('tabindex', '0')` and `el.setAttribute('role', 'button')`, then add a keydown listener that checks for `e.key === 'Enter' || e.key === ' '`.

## 2024-05-24 - Context-Aware Focus Restoration
**Learning:** Simply calling `.focus()` on a saved `lastFocusedElement` isn't enough if that element might be hidden (e.g., inside a navigation overlay that just closed).

**Action:** Implement a `restoreFocus()` utility that checks if the target element is still visible/valid before focusing, or defaults to a safe fallback like the `burgerBtn`.
