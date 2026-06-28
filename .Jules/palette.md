## 2025-05-14 - [A11y Pattern: Focus Management in Overlays]
**Learning:** For a site with `cursor: none`, `:focus-visible` is the only visual feedback for keyboard users. Programmatic focus restoration (storing `activeElement` before opening modals and restoring it on close) is essential for a seamless non-mouse experience.
**Action:** Always store `lastFocusedElement` when opening overlays and implement a `restoreFocus()` helper called by all close triggers (Escape, buttons, background clicks).
