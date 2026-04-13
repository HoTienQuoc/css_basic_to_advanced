Thuộc tính **`float`** trong CSS dùng để **đẩy một phần tử sang trái hoặc phải**, và cho phép **text hoặc inline elements bao quanh nó** 🧭

---

## 🧩 Cách hoạt động của `float`

* Khi một phần tử dùng `float`, nó **bị loại khỏi luồng bình thường (normal flow)** của trang.
* Các phần tử khác (đặc biệt là text) sẽ **bao quanh** phần tử đó.
* Nó **khác với `position: absolute`** vì vẫn ảnh hưởng bố cục xung quanh.

---

## 🧪 Cú pháp cơ bản

```css
float: left;
float: right;
float: none;
float: inline-start;
float: inline-end;
```

---

## 📌 Các giá trị phổ biến

* `left` → đẩy phần tử sang trái ⬅️
* `right` → đẩy phần tử sang phải ➡️
* `none` → không float (mặc định)
* `inline-start` → đầu dòng (trái với LTR, phải với RTL)
* `inline-end` → cuối dòng (phải với LTR, trái với RTL)

---

## 🔧 Ví dụ đơn giản

```html
<img src="avatar.png" class="avatar">
<p>
  Đây là đoạn text sẽ bao quanh hình ảnh khi float.
</p>
```

```css
.avatar {
  float: left;
  margin-right: 10px;
}
```

👉 Kết quả: ảnh nằm bên trái, text chạy quanh bên phải.

---

## ⚠️ Lưu ý quan trọng

* Phần tử `float` **không làm cha tự giãn chiều cao**
* Vì vậy thường phải dùng `clear` hoặc clearfix.

Ví dụ:

```css
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```

---

## 🧠 Float ảnh hưởng đến display

Một số phần tử khi `float` sẽ tự chuyển sang dạng block:

* `inline` → `block`
* `inline-block` → `block`
* `inline-flex` → `flex`
* `inline-grid` → `grid`

---

## 📊 Khi nào dùng `float`

* Bọc text quanh ảnh 🖼️
* Layout kiểu cũ (trước khi có flexbox/grid)
* Nội dung báo chí/blog

---

## 🚫 Khi nào KHÔNG nên dùng

Ngày nay nên dùng:

* `display: flex` 🔥
* `display: grid` 🔥

`float` giờ chủ yếu dùng cho **wrap text quanh ảnh** thôi.

---

## So sánh nhanh

| Thuộc tính | Dùng cho layout | Wrap text |
| ---------- | --------------- | --------- |
| float      | ⚠️ cũ           | ✅         |
| flexbox    | ✅               | ❌         |
| grid       | ✅               | ❌         |

---

Nếu bạn đang học CSS layout (media query, clamp… như các câu trước của bạn), thì:
👉 **float là kiến thức nền**, nhưng thực tế bạn nên dùng **flexbox** nhiều hơn.
