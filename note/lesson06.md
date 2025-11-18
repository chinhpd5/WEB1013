# Pseudo-class, Liên kết & Menu đơn giản

Mục tiêu buổi học
- Hiểu và sử dụng `pseudo-class` như `:hover`, `:active`, `:focus`, `:visited`
- Định dạng thẻ `<a>` – liên kết HTML bằng CSS
- Thiết kế menu ngang cơ bản bằng `CSS`
- Tăng tính tương tác cho `website` (`hover`, `click`...)


## Pseudo-class là gì?
Là các trạng thái đặc biệt của phần tử `HTML` khi người dùng tương tác
```css
selector:pseudo-class {
  property: value;
}
```

## Một số pseudo-class thường dùng
| **Pseudo-class** | **Ý nghĩa / Ứng dụng**                      |
| ---------------- | ------------------------------------------- |
| `:hover`         | Khi rê chuột vào phần tử                    |
| `:active`        | Khi phần tử đang được nhấn                  |
| `:focus`         | Khi phần tử được focus (ô input, button...) |
| `:visited`       | Link đã được truy cập                       |
| `:first-child`   | Áp dụng cho phần tử con đầu tiên (nâng cao) |


## Ví dụ định dạng liên kết <a>
```html
<a href="https://fpt.edu.vn">Trang FPT</a>
```

```css
a {
  color: blue;
  text-decoration: none;
}

a:hover {
  color: red;
  text-decoration: underline;
}

a:visited {
  color: purple;
}
```

## Pseudo-class với nút và input

```html
<input type="text" placeholder="Nhập tên">
<button>Gửi</button>
```

```css
input:focus {
  border: 2px solid blue;
  background-color: #f0f8ff;
}

button:hover {
  background-color: green;
  color: white;
}
```

Bài tập:
```html
<!-- Thẻ thông tin -->
<div class="card">
  <img src="https://via.placeholder.com/100" alt="avatar">
  <h3>Nguyễn Văn A</h3>
  <button>Xem thêm</button>
</div>

<!-- Menu -->
<nav class="menu">
  <a href="#">Trang chủ</a>
  <a href="#">Giới thiệu</a>
  <a href="#">Liên hệ</a>
  <a href="#">Tài khoản</a>
</nav>
```
- Phần 1: Thẻ thông tin người dùng
Tạo một thẻ người dùng gồm:
+ Ảnh đại diện hình tròn, bo viền căn giữa
+ Tên người dùng căn giữa, in đậm
+ Nút `"Xem thêm"`

Yêu cầu kỹ thuật, 
Khi rê chuột (:hover) vào thẻ:
+ Đổi màu nền
+ Đổi màu chữ
Khi rê chuột vào nút:
+ Đổi màu nền
+ Đổi màu chữ
Khi click nút (:active),
+ Đổi màu nền sang màu tối hơn

- Phần 2: Menu liên kết
Tạo một menu ngang gồm 4 liên kết:
+ Trang chủ
+ Giới thiệu
+ Liên hệ
+ Tài khoản
Yêu cầu kỹ thuật:
+ chiều ngang toàn màn hình, chiều dọc `50px`, căn giữa 2 chiều
+ Có màu nền, chữ, căn giữa, bỏ gạch chân, in đậm
Khi hover vào liên kết:
+ Đổi màu chữ, màu nền
