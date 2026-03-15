# CSS Animations & Transitions

## Transitions
Simple state change animations.
```css
.btn {
  transition: background-color 0.3s ease-in-out;
}
.btn:hover {
  background-color: blue;
}
```

## Keyframes
Complex, multi-step animations.
```css
@keyframes slideIn {
  from {
    transform: translateX(-100%);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}

.box {
  animation: slideIn 0.5s forwards;
}
```

## Shortcuts (Shorthand)
- `transition: <prop> <duration> <timing> <delay>;`
- `animation: <name> <duration> <timing> <delay> <count> <direction> <fill-mode>;`

## Transform Basics
- `translate(x, y)`: Move element.
- `scale(x, y)`: Resize element.
- `rotate(deg)`: Rotate element.
- `skew(deg, deg)`: Distortion.
