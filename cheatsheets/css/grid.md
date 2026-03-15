# CSS Grid

Grid is a two-dimensional layout system for the web.

## Container Properties
- `display: grid | inline-grid;`
- `grid-template-columns: <track-size> ... | <line-name> <track-size> ...;`
- `grid-template-rows: <track-size> ... | <line-name> <track-size> ...;`
- `grid-template-areas: "area-name | . | none" ...;`
- `grid-column-gap: <line-size>;`
- `grid-row-gap: <line-size>;`
- `grid-gap: <grid-row-gap> <grid-column-gap>;` (Shorthand)
- `justify-items: start | end | center | stretch;` (Along row axis)
- `align-items: start | end | center | stretch;` (Along column axis)
- `place-items: <align-items> <justify-items>;` (Shorthand)
- `justify-content: start | end | center | stretch | space-around | space-between | space-evenly;`
- `align-content: start | end | center | stretch | space-around | space-between | space-evenly;`
- `place-content: <align-content> <justify-content>;` (Shorthand)

## Item Properties
- `grid-column-start: <number> | <name> | span <number> | span <name> | auto;`
- `grid-column-end: <number> | <name> | span <number> | span <name> | auto;`
- `grid-column: <start-line> / <end-line>;` (Shorthand)
- `grid-row: <start-line> / <end-line>;` (Shorthand)
- `grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>;`
- `justify-self: start | end | center | stretch;`
- `align-self: start | end | center | stretch;`
- `place-self: <align-self> <justify-self>;` (Shorthand)

## Helpful Units / Functions
- `fr`: Fraction of available space.
- `repeat(times, size)`: Reiterate track definitions.
- `minmax(min, max)`: Defines a size range.
- `auto-fill`, `auto-fit`: Keywords for responsive columns.
