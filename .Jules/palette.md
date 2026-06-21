## 2025-05-14 - Accessible Infinite Grids with DOM Recycling
**Learning:** In infinite scroll systems that recycle DOM nodes (like virtualized grids), accessibility metadata such as `aria-label` or `aria-description` must be synchronized within the recycling/rendering loop. If these attributes are only set once during initial element creation, screen readers will announce stale information when the node is visually repurposed for new content.
**Action:** Always include ARIA attribute updates in the same logic that updates `src`, `innerText`, or other content properties during DOM recycling.

## 2025-05-14 - Keyboard Parity for Custom Interactive Elements
**Learning:** When using `div` elements as interactive gallery items, full keyboard accessibility requires `tabindex="0"`, `role="button"`, and explicit `keydown` listeners for 'Enter' and 'Space' keys. Using `e.preventDefault()` on Space is necessary to prevent the default page scroll behavior while activating the element.
**Action:** Use a consistent utility or pattern to apply these three pillars (tabindex, role, listeners) to any custom interactive component.
