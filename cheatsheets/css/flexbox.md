# CSS Flexbox

Flexbox is a one-dimensional layout method for arranging items in rows or columns.

## Container Properties
- `display: flex | inline-flex;`
- `flex-direction: row | row-reverse | column | column-reverse;`
- `flex-wrap: nowrap | wrap | wrap-reverse;`
- `justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;` (Main axis)
- `align-items: stretch | flex-start | flex-end | center | baseline;` (Cross axis)
- `align-content: flex-start | flex-end | center | space-between | space-around | stretch;` (Multi-line)
- `gap: <value>;` (Shorthand for row-gap and column-gap)

## Item Properties
- `flex-grow: <number>;` (Default: 0)
- `flex-shrink: <number>;` (Default: 1)
- `flex-basis: <length> | auto;` (Default: auto)
- `flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]` (Shorthand)
- `align-self: auto | flex-start | flex-end | center | baseline | stretch;`
- `order: <integer>;` (Default: 0)

## Centering Cheat
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```
