# CSS Selectors & Specificity

## Selectors
- `*`: Universal selector.
- `div`: Type selector.
- `.class`: Class selector.
- `#id`: ID selector.
- `[type="text"]`: Attribute selector.
- `div p`: Descendant combinator.
- `div > p`: Child combinator (direct).
- `div + p`: Adjacent sibling combinator.
- `div ~ p`: General sibling combinator.

## Pseudo-classes
- `:hover`, `:active`, `:focus`.
- `:nth-child(n)`, `:first-child`, `:last-child`.
- `:not(.special)`.

## Specificity Hierarchy
Calculated by (ID, Class/Attribute/Pseudo, Type):
1.  **Inline styles**: `1, 0, 0, 0`
2.  **IDs**: `0, 1, 0, 0`
3.  **Classes, attributes, and pseudo-classes**: `0, 0, 1, 0`
4.  **Elements and pseudo-elements**: `0, 0, 0, 1`

**Tip**: Use Classes instead of IDs for styling to keep specificity manageable. Avoid `!important`.

## Box Model (Quick Tip)
```css
* { box-sizing: border-box; }
```
Width = content + padding + border.
