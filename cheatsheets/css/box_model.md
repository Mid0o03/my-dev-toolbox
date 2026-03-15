# CSS Box Model

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

## Components
- **Content**: The content of the box, where text and images appear.
- **Padding**: Clears an area around the content. The padding is transparent.
- **Border**: A border that goes around the padding and content.
- **Margin**: Clears an area outside the border. The margin is transparent.

## Box Sizing
- `box-sizing: content-box;` (Default): Width and height include only the content. Padding and border are added outside.
- `box-sizing: border-box;`: Width and height include content, padding, and border. **Highly recommended.**

```css
* {
  box-sizing: border-box;
}
```

## Total Size Calculation (content-box)
- Total Width = width + left padding + right padding + left border + right border + left margin + right margin
- Total Height = height + top padding + bottom padding + top border + bottom border + top margin + bottom margin
