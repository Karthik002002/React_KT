# 📘 HTML Semantics vs Non-Semantics Elements

Understanding **semantic** and **non-semantic** elements is essential for writing clean, accessible, and maintainable HTML code.

---

## ✅ Semantic HTML Elements

**Definition:**  
Semantic elements clearly describe their meaning in a human- and machine-readable way. These tags give **meaning** to the content they wrap and help search engines, screen readers, and developers understand the structure of the webpage.

### 📌 Common Semantic Elements:

| Element        | Purpose                                                  |
| -------------- | -------------------------------------------------------- |
| `<header>`     | Defines a header for a page or section                   |
| `<nav>`        | Defines a container for navigation links                 |
| `<main>`       | Represents the main content of the document              |
| `<section>`    | Represents a standalone section of content               |
| `<article>`    | Represents a self-contained composition                  |
| `<aside>`      | Represents content aside from the main content           |
| `<footer>`     | Defines a footer for a page or section                   |
| `<figure>`     | Wraps media (like images) and their captions             |
| `<figcaption>` | Caption for the `<figure>` element                       |
| `<time>`       | Represents a specific time (date/time)                   |
| `<mark>`       | Highlights text                                          |
| `<address>`    | Provides contact information                             |
| `<details>`    | Container for additional details the user can open/close |
| `<summary>`    | Defines a summary for the `<details>` element            |
| `<dialog>`     | Represents a dialog box or window                        |

---

## ❌ Non-Semantic HTML Elements

**Definition:**  
Non-semantic elements **do not convey any specific meaning** about the content inside them. They are used for layout or styling purposes only.

### 📌 Common Non-Semantic Elements:

| Element    | Purpose                                           |
| ---------- | ------------------------------------------------- |
| `<div>`    | Generic container for block-level content         |
| `<span>`   | Generic container for inline content              |
| `<b>`      | Makes text bold, without implying importance      |
| `<i>`      | Makes text italic, without emphasizing importance |
| `<font>`   | Defines font size, color, and face _(deprecated)_ |
| `<center>` | Centers content horizontally _(deprecated)_       |

---

## ⚖️ Summary Comparison

| Feature           | Semantic Elements | Non-Semantic Elements |
| ----------------- | ----------------- | --------------------- |
| Meaningful markup | ✅ Yes            | ❌ No                 |
| Accessibility     | ✅ Improved       | ❌ Poor               |
| SEO-friendly      | ✅ Yes            | ❌ No                 |
| Styling only      | ❌ No             | ✅ Yes                |

---

## 📌 Notes

- Use **semantic elements** whenever possible to improve accessibility and SEO.
- Avoid deprecated non-semantic tags like `<font>` and `<center>` in modern HTML.
