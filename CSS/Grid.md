
# CSS Grid Guide

CSS Grid Layout is a two-dimensional layout system for the web. It allows developers to design web pages using rows and columns.

---

## 🔧 Basics

To use Grid, set the container’s `display` to `grid` or `inline-grid`:

```css
.container {
  display: grid;
}
```

All direct children become **grid items**.

---

## 📐 Main Properties

### 1. `grid-template-columns` & `grid-template-rows`
Defines the number and size of columns and rows.

```css
.container {
  grid-template-columns: 100px 100px 100px;
  grid-template-rows: auto auto;
}
```

Or use `repeat()` and `fr` units:

```css
.container {
  grid-template-columns: repeat(3, 1fr);
}
```

---

### 2. `grid-gap` (or `gap`)
Sets the space between rows and columns.

```css
.container {
  gap: 10px;
}
```

---

### 3. `grid-column` & `grid-row`
Controls item placement and span across columns/rows.

```css
.item {
  grid-column: 1 / 3;
  grid-row: 1 / 2;
}
```

---

### 4. `grid-area`
Assigns a name to an item and can be used with `grid-template-areas`.

```css
.item {
  grid-area: header;
}
```

```css
.container {
  grid-template-areas:
    "header header"
    "sidebar content";
}
```

---

## 🧭 Alignment

### `justify-items` & `align-items`
Align items within their grid area.

```css
.container {
  justify-items: center;
  align-items: stretch;
}
```

### `justify-content` & `align-content`
Align the entire grid within the container.

```css
.container {
  justify-content: center;
  align-content: space-between;
}
```

---

## ⚙️ Shorthand: `grid`

Shorthand for setting all grid properties:

```css
.container {
  display: grid;
  grid: auto / auto auto auto;
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
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}

.item {
  background-color: lightgreen;
  padding: 20px;
  text-align: center;
}
```

---

## 📚 Resources

- [MDN Web Docs - Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)
- [CSS Tricks - Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)

---

> 💡 Grid is best for complex, two-dimensional layouts that require precise control over both rows and columns.
