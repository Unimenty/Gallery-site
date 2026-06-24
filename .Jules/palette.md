## 2025-05-14 - Defensive Global Listeners
**Learning:** Global 'keydown' handlers (e.g., for 'Escape') must use existence checks or optional chaining (`?.`) for all referenced DOM elements to ensure script stability across different pages where specific elements might be absent.
**Action:** Always wrap DOM manipulations in existence checks (`if (el) ...`) or use optional chaining in global scope listeners.

## 2025-05-14 - UX Pattern: Keyboard Accessibility for Grid Items
**Learning:** To enable keyboard accessibility on custom grid items concisely, assign `tabindex="0"` and `role="button"`, then use `el.addEventListener('keydown', e => (e.key === 'Enter' || e.key === ' ') && (e.preventDefault(), el.click()))` to support both activation keys while suppressing scroll.
**Action:** Apply this pattern to all interactive non-semantic elements.
