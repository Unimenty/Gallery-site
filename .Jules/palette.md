## 2026-06-29 - [A11y/UX] Enhanced Keyboard Accessibility and Focus Management
**Learning:** Implementing programmatic focus management (using tabindex="-1" on containers) and focus restoration is crucial for maintaining a coherent experience for keyboard users in dynamic portfolios with multiple overlays.
**Action:** Always track 'lastFocusedElement' before opening overlays and ensure 'Escape' key support is globally available to restore the user's previous context.
