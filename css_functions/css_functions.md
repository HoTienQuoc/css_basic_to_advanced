Dưới đây là tài liệu `.md` giải thích ngắn gọn từng hàm CSS bạn liệt kê, kèm ví dụ và kết quả 👇

---

# 📘 CSS Functions Cheat Sheet

## 🔢 Math & Numeric Functions

### `abs()`

**Lý thuyết:** Trả về giá trị tuyệt đối.
**Ví dụ:**

```css
width: abs(-50px);
```

**Kết quả:** `50px`

---

### `acos()`

**Lý thuyết:** Trả về arccos (radian).

```css
transform: rotate(acos(0.5));
```

**Kết quả:** ~1.047rad (60°)

---

### `asin()`

**Lý thuyết:** Arcsin.

```css
transform: rotate(asin(1));
```

**Kết quả:** ~1.57rad (90°)

---

### `atan()`

**Lý thuyết:** Arctan.

```css
transform: rotate(atan(1));
```

**Kết quả:** ~45°

---

### `atan2(y, x)`

**Lý thuyết:** Góc từ tọa độ (y, x).

```css
transform: rotate(atan2(1, 1));
```

**Kết quả:** 45°

---

### `calc()`

**Lý thuyết:** Tính toán động.

```css
width: calc(100% - 50px);
```

**Kết quả:** Chiều rộng = 100% - 50px

---

### `clamp(min, val, max)`

**Lý thuyết:** Giới hạn giá trị.

```css
font-size: clamp(16px, 5vw, 32px);
```

**Kết quả:** Luôn nằm trong [16px, 32px]

---

### `max()` / `min()`

```css
width: max(300px, 50%);
```

👉 Lấy giá trị lớn hơn

---

### `round()`

**Lý thuyết:** Làm tròn.

```css
width: round(12.7px);
```

👉 `13px`

---

### `sqrt()`

```css
width: sqrt(16px);
```

👉 `4px`

---

## 🎨 Color Functions

### `rgb()`

```css
color: rgb(255, 0, 0);
```

👉 Màu đỏ

---

### `hsl()`

```css
color: hsl(120, 100%, 50%);
```

👉 Màu xanh lá

---

### `color-mix()`

**Lý thuyết:** Trộn màu

```css
color: color-mix(in srgb, red 50%, blue);
```

👉 Tím

---

### `oklab()` / `oklch()`

👉 Hệ màu hiện đại, chính xác hơn RGB

---

### `light-dark()`

```css
color: light-dark(black, white);
```

👉 Tự đổi theo dark mode

---

## 🌈 Gradient Functions

### `linear-gradient()`

```css
background: linear-gradient(red, blue);
```

👉 Gradient dọc

---

### `radial-gradient()`

```css
background: radial-gradient(circle, red, blue);
```

👉 Gradient tròn

---

### `conic-gradient()`

```css
background: conic-gradient(red, blue);
```

👉 Gradient xoay tròn

---

## 🖼 Image Functions

### `url()`

```css
background-image: url("image.jpg");
```

---

### `image-set()`

```css
background-image: image-set("img.png" 1x, "img@2x.png" 2x);
```

👉 Responsive ảnh

---

### `cross-fade()`

👉 Trộn 2 ảnh

---

## 🔷 Shape Functions

### `circle()`

```css
clip-path: circle(50%);
```

---

### `ellipse()`

```css
clip-path: ellipse(50% 30%);
```

---

### `polygon()`

```css
clip-path: polygon(0 0, 100% 0, 50% 100%);
```

---

### `path()`

👉 Vẽ SVG path

---

## 🔄 Transform Functions

### `rotate()`

```css
transform: rotate(45deg);
```

---

### `scale()`

```css
transform: scale(2);
```

---

### `translate()`

```css
transform: translateX(50px);
```

---

### `skew()`

```css
transform: skew(20deg);
```

---

### `matrix()`

👉 Transform nâng cao

---

## 🔆 Filter Functions

### `blur()`

```css
filter: blur(5px);
```

---

### `brightness()`

```css
filter: brightness(150%);
```

---

### `contrast()`

```css
filter: contrast(200%);
```

---

### `drop-shadow()`

```css
filter: drop-shadow(2px 2px 5px black);
```

---

## 🧠 Logic & Variables

### `var()`

```css
color: var(--main-color);
```

---

### `env()`

👉 Lấy biến môi trường (safe-area)

---

### `attr()`

```css
content: attr(data-name);
```

---

## 🧮 Advanced / Experimental

### `hypot()`

👉 Tính độ dài vector

```css
width: hypot(3px, 4px);
```

👉 `5px`

---

### `pow()`

```css
width: pow(2, 3);
```

👉 `8`

---

### `log()`

👉 Logarithm

---

### `exp()`

👉 e^x

---

### `random()`

👉 Random số

---

### `if()`

👉 Điều kiện CSS (experimental)

---

## 📦 Layout Functions

### `fit-content()`

```css
width: fit-content(200px);
```

---

### `minmax()`

```css
grid-template-columns: minmax(100px, 1fr);
```

---

## 🎭 Animation Timing

### `cubic-bezier()`

```css
transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
```

---

### `steps()`

```css
animation-timing-function: steps(4);
```

---

## 📊 Counters

### `counter()`

```css
content: counter(section);
```

---

### `counters()`

👉 Nhiều cấp

---

## 📐 Geometry

### `inset()`

```css
clip-path: inset(10px);
```

---

### `rect()` *(deprecated)*

👉 Dùng thay bằng `inset()`

---

## ⚠️ Deprecated / Non-standard

* `-moz-image-rect` ❌ (deprecated)

---

# 📌 Tổng kết

* Nhóm **Math**: `calc`, `clamp`, `sin`, `cos`
* Nhóm **Color**: `rgb`, `hsl`, `color-mix`
* Nhóm **Transform**: `rotate`, `scale`
* Nhóm **Filter**: `blur`, `brightness`
* Nhóm **Shape**: `circle`, `polygon`
* Nhóm **Experimental**: `if`, `random`

---

Nếu bạn muốn, mình có thể:
✅ Tạo mindmap dễ nhớ
✅ Phân loại theo level (junior → senior)
✅ Hoặc làm bài tập thực hành cho từng nhóm 🚀
