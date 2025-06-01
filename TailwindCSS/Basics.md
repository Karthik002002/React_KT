# 🐦 Tailwind CSS Complete Cheatsheet

A utility-first CSS framework for rapidly building custom UIs.

---

## 📦 Installation

```bash
npm install -D tailwindcss
npx tailwindcss init
```

### Configure `tailwind.config.js`

```js
module.exports = {
  content: ["./src/**/*.{html,js,jsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

### Include in CSS

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 🄤 Typography

| Class         | Description                |
| ------------- | -------------------------- |
| `text-xs`     | Extra small text           |
| `text-sm`     | Small text                 |
| `text-lg`     | Large text                 |
| `text-xl`     | Extra large text           |
| `font-bold`   | Bold text                  |
| `font-light`  | Light text                 |
| `text-center` | Center-aligned text        |
| `truncate`    | Truncates text w/ ellipsis |

---

## 🎨 Colors

```html
<div class="bg-blue-500 text-white">Button</div>
```

* **Background**: `bg-{color}-{intensity}`
* **Text**: `text-{color}-{intensity}`
* **Border**: `border-{color}-{intensity}`

Popular colors: `gray`, `blue`, `red`, `green`, `yellow`, `purple`, etc.

---

## 📏 Spacing (Margin & Padding)

| Type    | Class Example | Description           |
| ------- | ------------- | --------------------- |
| Padding | `p-4`, `px-2` | `p`, `px`, `py`, etc. |
| Margin  | `m-4`, `my-1` | `m`, `mx`, `my`, etc. |

---

## 📊 Layout & Sizing

* Width: `w-full`, `w-1/2`, `w-64`
* Height: `h-screen`, `h-16`
* Max-width: `max-w-sm`, `max-w-md`
* Display: `block`, `inline-block`, `hidden`

---

## 🧰 Flexbox

```html
<div class="flex justify-between items-center">...</div>
```

| Class                  | Description           |
| ---------------------- | --------------------- |
| `flex`                 | Enables Flexbox       |
| `flex-row`, `flex-col` | Direction             |
| `justify-center`       | Horizontal alignment  |
| `items-center`         | Vertical alignment    |
| `gap-4`                | Spacing between items |
| `flex-wrap`            | Wrap child elements   |

---

## 🪟 Grid

```html
<div class="grid grid-cols-3 gap-4">...</div>
```

| Class                | Description           |
| -------------------- | --------------------- |
| `grid`               | Display grid          |
| `grid-cols-{n}`      | Set number of columns |
| `grid-rows-{n}`      | Set number of rows    |
| `col-span-{n}`       | Span columns          |
| `gap-4`              | Gap between rows/cols |
| `place-items-center` | Center items          |

---

## 🎮 Animation & Transitions

```html
<div class="transition-all duration-300 ease-in-out hover:scale-105">
  Hover Me
</div>
```

| Class                 | Description           |
| --------------------- | --------------------- |
| `transition`          | Enable transition     |
| `duration-500`        | Set duration in ms    |
| `ease-in`, `ease-out` | Easing functions      |
| `hover:`              | Apply styles on hover |
| `animate-bounce`      | Predefined animation  |

---

## 🌐 Responsive Design

```html
<div class="text-sm md:text-lg lg:text-xl">Text</div>
```

| Prefix | Screen Width |
| ------ | ------------ |
| `sm:`  | ≥ 640px      |
| `md:`  | ≥ 768px      |
| `lg:`  | ≥ 1024px     |
| `xl:`  | ≥ 1280px     |

---

## 🏠 Example Component

```html
<button class="px-4 py-2 bg-indigo-600 text-white rounded hover:bg-indigo-700">
  Click Me
</button>
```

---

## 📚 Resources

* [Tailwind Docs](https://tailwindcss.com/docs)
* [Tailwind Play](https://play.tailwindcss.com/)
* [Tailwind Cheat Sheet](https://nerdcave.com/tailwind-cheat-sheet)

> 💡 Tip: Use JIT mode for blazing fast builds and extended utility generation.
