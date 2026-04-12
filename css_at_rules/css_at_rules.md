## 🎯 CSS at-rules là gì?

**CSS at-rules** là các câu lệnh bắt đầu bằng ký tự `@`, dùng để **hướng dẫn CSS cách hoạt động** hoặc **tổ chức stylesheet**.

👉 Chúng không áp dụng style trực tiếp cho phần tử như selector (`div`, `.class`…), mà **điều khiển cách CSS được xử lý**.

---

### 📘 Dịch sát nghĩa đoạn bạn đưa

* **At-rules** là các câu lệnh CSS hướng dẫn CSS cách hoạt động.
* Chúng được dùng để:

  * Nhóm và cấu trúc các rule CSS và at-rule khác
  * Khai báo thông tin style không gắn trực tiếp với phần tử
  * Quản lý cú pháp như `import`, `namespace`
* Chúng **bắt đầu bằng ký hiệu `@`** theo sau là một định danh.

---

## 🧠 Ví dụ đơn giản

```css
@import url("style.css");

@media (max-width: 768px) {
  body {
    background: lightblue;
  }
}
```

👉 `@import` và `@media` đều là **at-rules**

---

# 📚 Các CSS at-rules phổ biến nhất

### 1. `@import` – import file CSS

```css
@import url("style.css");
```

### 2. `@media` – responsive

```css
@media (max-width: 768px) {
  body { font-size: 14px; }
}
```

### 3. `@font-face` – custom font

```css
@font-face {
  font-family: "MyFont";
  src: url("font.woff2");
}
```

### 4. `@keyframes` – animation

```css
@keyframes fade {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

### 5. `@supports` – kiểm tra feature

```css
@supports (display: grid) {
  .grid { display: grid; }
}
```

---

# 🗂️ Phân loại dễ nhớ

### 🧩 Nhóm layout / responsive

* `@media`
* `@container`
* `@supports`
* `@layer`

### 🎨 Nhóm font

* `@font-face`
* `@font-feature-values`
* `@font-palette-values`

### 🎬 Nhóm animation

* `@keyframes`

### 📦 Nhóm import / cấu trúc

* `@import`
* `@namespace`
* `@charset`

### 🖨️ Nhóm print

* `@page`

---

# 📊 Media features (dùng trong `@media`)

Đây là các điều kiện bạn có thể dùng:

### Responsive kích thước

```css
@media (width: 768px) {}
@media (height: 600px) {}
```

### Orientation

```css
@media (orientation: landscape) {}
```

### Dark mode

```css
@media (prefers-color-scheme: dark) {}
```

### Hover support

```css
@media (hover: hover) {}
```

### Reduced motion

```css
@media (prefers-reduced-motion: reduce) {}
```

---

# 🚀 Ví dụ tổng hợp

```css
@import url("base.css");

@font-face {
  font-family: "MyFont";
  src: url("font.woff2");
}

@media (max-width: 768px) {
  body {
    font-size: 14px;
  }
}

@supports (display: grid) {
  .layout {
    display: grid;
  }
}
```

---

# 🧠 Nhớ nhanh

* `@` = CSS directive
* at-rules = điều khiển CSS
* selector = áp style trực tiếp

---

Bạn đang học CSS phần này để:

* làm responsive?
* chuẩn bị học `@container`?
* hay ôn CSS fundamentals?
