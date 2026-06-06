## 2025-05-15 - Global Focus Management & Keyboard Nav in Photography Portfolios
**Learning:** Custom 'Platinum Grid Engine' or virtualized galleries often omit keyboard support, making them inaccessible. Additionally, custom cursors that hide the default browser pointer also hide the default focus indicators, requiring explicit `:focus-visible` styles.
**Action:** Always implement focus trapping and restoration for overlays, add 'Enter'/'Space' listeners to custom grid items, and use high-contrast `:focus-visible` outlines to compensate for hidden cursors.
