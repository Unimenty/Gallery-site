## 2025-05-14 - Custom Cursor and Keyboard Accessibility
**Learning:** Custom hidden cursors (`cursor: none`) create a significant accessibility barrier by removing the visual cue for keyboard-only users. High-contrast `:focus-visible` outlines and programmatic cursor restoration are mandatory when using this pattern.
**Action:** Always pair `cursor: none` with a CSS rule that restores the cursor or provides a distinct focus indicator during keyboard interaction (e.g., using `:focus-visible`).
