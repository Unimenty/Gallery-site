## 2025-05-14 - [Aria State Synchronization on Overlay Closure]
**Learning:** When using global keyboard listeners (like 'Escape') to close custom UI components, it is crucial to manually synchronize their accessibility state (e.g., `aria-expanded`). Relying solely on visual class toggles leaves screen readers with stale information.
**Action:** Always include ARIA attribute updates in global event handlers that modify component visibility or state.

## 2025-05-14 - [Visual Feedback in Cursor-less Environments]
**Learning:** In luxury editorial designs where the default cursor is hidden (`cursor: none`), high-contrast `:focus-visible` outlines are the primary lifeline for keyboard-only users.
**Action:** Use `outline: 2px solid #fff` with appropriate `outline-offset` to ensure all interactive elements are clearly marked when focused, especially when the system cursor is missing.
