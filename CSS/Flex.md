
# CSS Flexbox Guide

CSS Flexbox is a layout model that allows elements to align and distribute space within a container, even when their size is unknown or dynamic.

---

## 🔧 Basics

To use Flexbox, set the container’s `display` to `flex` or `inline-flex`:

```css
.container {
  display: flex;
}
```

All direct children become **flex items**.

---

## 📐 Main Concepts

### 1. `flex-direction`
Defines the direction of the main axis.

```css
flex-direction: row | row-reverse | column | column-reverse;
```

- `row` (default): left to right
- `row-reverse`: right to left
- `column`: top to bottom
- `column-reverse`: bottom to top

---

### 2. `justify-content`
Aligns items **horizontally** along the main axis.

```css
justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
```

---

### 3. `align-items`
Aligns items **vertically** along the cross axis.

```css
align-items: stretch | flex-start | flex-end | center | baseline;
```

---

### 4. `flex-wrap`
Allows items to wrap onto multiple lines.

```css
flex-wrap: nowrap | wrap | wrap-reverse;
```

- `nowrap` (default): all items stay on one line
- `wrap`: items wrap onto multiple lines
- `wrap-reverse`: items wrap in reverse order

---

### 5. `align-content`
Aligns lines of items when wrapping.

```css
align-content: flex-start | flex-end | center | space-between | space-around | stretch;
```

---

## ⚙️ Flex Item Properties

### 1. `flex-grow`
Defines how much a flex item will grow relative to others.

```css
.item {
  flex-grow: 1;
}
```

---

### 2. `flex-shrink`
Defines how a flex item shrinks when space is tight.

```css
.item {
  flex-shrink: 1;
}
```

---

### 3. `flex-basis`
Specifies the initial size of a flex item before space distribution.

```css
.item {
  flex-basis: 100px;
}
```

---

### 4. `flex`
Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.

```css
.item {
  flex: 1 1 100px;
}
```

---

### 5. `align-self`
Overrides the `align-items` value for a specific flex item.

```css
.item {
  align-self: center;
}
```

---

## 🧪 Example

```html
<div class="container">
  <div class="item">A</div>
  <div class="item">B</div>
  <div class="item">C</div>
</div>
```

```css
.container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 100px;
}

.item {
  flex: 1;
  text-align: center;
  padding: 10px;
  background: lightblue;
}
```

---

## 📚 Resources

- [MDN Web Docs - Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
- [CSS Tricks - Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

---

> 💡 Flexbox is perfect for building responsive layouts without floats or positioning hacks.
