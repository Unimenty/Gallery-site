## 2026-07-08 - [Dynamic ARIA Management in Virtualized Grids]
**Learning:** In virtualized or infinite grids where DOM nodes are recycled (like the Platinum Grid Engine), static accessibility attributes (role, tabindex) are preserved, but state-specific metadata (aria-label, alt text) can become stale if not updated during the recycling loop.
**Action:** Always synchronize ARIA attributes within the grid's render/recycle function (e.g., `updateGridPatternIfNeeded`) to ensure screen readers receive accurate information as the user scrolls.

## 2026-07-08 - [Focus Restoration in Dynamic Contexts]
**Learning:** Closing a modal or lightbox in a complex, dynamic grid often causes focus to be lost or reset to the body, disorienting keyboard users.
**Action:** Implement a `lastFocusedElement` pattern to capture the triggering element before opening a modal and programmatically restore focus to it upon closing, ensuring a continuous and predictable navigation path.
