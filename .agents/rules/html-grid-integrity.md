---
description: Enforce strict HTML tag nesting and CSS Grid structural validation
globs: ["**/*.html", "**/*.jsx", "**/*.tsx"]
---

# HTML Tag Nesting & CSS Grid Structural Integrity

1. **Tag Nesting Validation**:
   - Always ensure every opening tag (`<strong>`, `<span>`, `<div>`, `<a>`, `<p>`) is strictly matched with its identical closing counterpart.
   - Never close an element with a mismatched tag (e.g., `<tag>...</other-tag>`).

2. **CSS Grid Item Isolation**:
   - In CSS Grid containers (`display: grid`, `grid-cols-*`), verify that all planned grid items are direct children of the grid container.
   - If grid items appear stacked, skipped, or misaligned, immediately check the preceding card or element for unclosed tags before changing CSS classes.

3. **Pre-commit Automated Audit**:
   - Run a DOM tag-nesting verification parser to confirm zero unclosed or orphaned tags before concluding tasks modifying HTML templates.
