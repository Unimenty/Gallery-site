# Palette's Journal

## 2025-05-15 - Focus Management in Dynamic Grid Overlays
**Learning:** In a high-fashion portfolio with a custom "Grid Engine" and multiple frosted-glass overlays (Lightbox, Nav Menu, Services), keyboard focus can easily get lost or stuck on hidden elements. Standard focus restoration (returning focus to the button that opened the modal) is essential, but must also account for automatic menu closures (e.g., clicking a link within the menu). Using a global `lastFocusedElement` state variable and ensuring all modal containers have `tabindex="-1"` allows for consistent programmatic focus control.
**Action:** Always implement a centralized `saveFocus` and `restoreFocus` pattern. Ensure dynamic items (like virtualized grid images) are manually assigned `tabindex="0"` and `role="button"` during their creation/recycling cycle, and that the global `Escape` handler respects the presence/absence of specific active components.
