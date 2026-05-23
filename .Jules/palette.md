## 2024-05-23 - Accessibility in Cursorless Interfaces
**Learning:** High-fashion portfolios often use `cursor: none` for a "luxury" aesthetic, but this completely breaks keyboard navigation because focus indicators are often overlooked or hidden along with the cursor. Focus-management is critical here to ensure users don't "get lost" when overlays close.
**Action:** Always implement `*:focus-visible` outlines and a `lastFocusedElement` restoration pattern when the system cursor is suppressed.

## 2024-05-23 - Concise Keyboard Support for Custom Grids
**Learning:** For infinite or custom grids, the most line-efficient way to add keyboard support without refactoring large click handlers is to use `el.tabIndex = 0` and a one-line keydown listener that calls `el.click()`.
**Action:** Use `e.key === 'Enter' && el.click()` to bridge keyboard interaction to existing UI logic under tight line-count constraints.
