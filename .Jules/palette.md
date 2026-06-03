## 2025-05-14 - Accessibility & Keyboard Navigation
**Learning:** Static site overlays (modals, nav menus) require explicit focus management (saving last focused element, setting tabindex="-1" on containers, and calling .focus()) to be accessible to keyboard and screen reader users. Global 'Escape' listeners and 'aria-expanded' states are critical for a polished UX.
**Action:** Always implement a 'lastFocusedElement' pattern and ensure all interactive overlays have appropriate ARIA roles and keyboard shortcuts.
