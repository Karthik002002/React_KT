
# 🎞️ CSS Animation Guide

CSS Animations allow elements to transition between styles over time, adding dynamic and interactive effects without JavaScript.

---

## 🔧 Basics

### 1. `transition` (for simple state changes)
Used for hover, focus, or active changes.

```css
.button {
  background-color: blue;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: darkblue;
}
```

---

### 2. `@keyframes` + `animation` (for complex animations)

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

.element {
  animation: slideIn 1s ease-in-out forwards;
}
```

---

## 🧩 Animation Properties

- `animation-name`: Name of the keyframes to apply.
- `animation-duration`: Time the animation runs.
- `animation-timing-function`: Easing method (`ease`, `linear`, `ease-in-out`, etc.).
- `animation-delay`: Delay before starting.
- `animation-iteration-count`: Number of repeats (`infinite` or `1`, `2`, etc.).
- `animation-direction`: Direction (`normal`, `reverse`, `alternate`).
- `animation-fill-mode`: Defines the style when not playing (`forwards`, `backwards`, etc.).

### Example:

```css
.element {
  animation: slideIn 2s ease-in-out 0.5s 1 normal forwards;
}
```

---

## 🧪 Example

```html
<div class="box"></div>
```

```css
.box {
  width: 100px;
  height: 100px;
  background: coral;
  animation: moveUp 1s ease-in-out infinite alternate;
}

@keyframes moveUp {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-50px);
  }
}
```

---

## 🧠 Tips

- Combine multiple animations with commas.
- Use `will-change` to hint performance improvement.
- Keep animations subtle for UX — avoid making users dizzy!

---

## 📚 Resources

- [MDN - CSS Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations)
- [CSS Tricks - Animation Guide](https://css-tricks.com/almanac/properties/a/animation/)
- [Animista](https://animista.net/) – Online CSS animation generator

---

> 💡 Use animations to enhance UX, guide user attention, and provide feedback — not just for decoration.
