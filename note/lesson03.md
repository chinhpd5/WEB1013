# Các thẻ Nâng cao - Thẻ ngữ nghĩa

Mục tiêu bài học:
- Tìm hiểu và thực hành các thẻ `table`, `form`
- Tìm hiểu các thẻ ngữ nghĩa


## Thẻ nâng cao

---
### HTML div - thẻ tạo khối
- Thẻ `<div>` (viết tắt của division) là thẻ khối dùng để nhóm nhiều phần tử `HTML` lại với nhau thành một khối.
- `<div>` không có ý nghĩa ngữ nghĩa riêng, chỉ dùng để tổ chức, bố cục, chia vùng giao diện.
- Thường được dùng kèm với `CSS` để thiết kế, canh lề, chia cột, tạo `layout`.

```html
<div>
  <h2>Thông tin sinh viên</h2>
  <p>Họ tên: Nguyễn Văn A</p>
  <p>Lớp: WEB1013</p>
</div>
```

---
### HTML Tables - Thẻ tạo bảng
Dùng tạo bảng

```html
<table border="1" cellpadding="8" cellspacing="0" align="center">
  <thead>
    <tr>
      <th>STT</th>
      <th>Họ tên</th>
      <th>Lớp</th>
      <th>Điểm giữa kỳ</th>
      <th>Điểm cuối kỳ</th>
      <th>Tổng kết</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Nguyễn Văn A</td>
      <td>WEB123</td>
      <td>7.5</td>
      <td>8.0</td>
      <td>7.8</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Trần Thị B</td>
      <td>WEB123</td>
      <td>6.0</td>
      <td>9.0</td>
      <td>7.5</td>
    </tr>
    <tr>
      <td colspan="6" style="text-align: center;"><em>Đã có 2 sinh viên nhập điểm</em></td>
    </tr>
  </tbody>
</table>
```

---
### HTML Form - Thẻ tạo biểu mẫu nhập liệu
- Thẻ `<form>` được dùng để tạo biểu mẫu `(form)` trên `website`, cho phép người dùng nhập dữ liệu và gửi lên máy chủ `(server)`.
- Ví dụ: đăng ký tài khoản, đăng nhập, gửi liên hệ, tìm kiếm, v.v.

```html
<form action="đường_dẫn_xử_lý" method="POST">
  <!-- Các trường nhập liệu -->
  <input type="text" name="username">
  <input type="submit" value="Gửi">
</form>
```

| Thẻ                     | Công dụng                   | Ví dụ                                   |
| ----------------------- | --------------------------- | --------------------------------------- |
| `<input>`               | Trường nhập liệu đơn dòng   | `<input type="text">`                   |
| `<textarea>`            | Trường nhập liệu nhiều dòng | `<textarea rows="4"></textarea>`        |
| `<select>` & `<option>` | Danh sách chọn              | `<select><option>Nam</option></select>` |
| `<button>`              | Nút bấm tùy chỉnh           | `<button>Gửi</button>`                  |
| `<label>`               | Nhãn mô tả cho input        | `<label for="name">Họ tên:</label>`     |

| Loại input | Cú pháp ví dụ                                        | Mục đích                    |
| ---------- | ---------------------------------------------------- | --------------------------- |
| `text`     | `<input type="text" name="hoten">`                   | Nhập chữ (1 dòng)           |
| `email`    | `<input type="email" name="email">`                  | Nhập địa chỉ email          |
| `password` | `<input type="password" name="matkhau">`             | Nhập mật khẩu               |
| `radio`    | `<input type="radio" name="gioitinh" value="Nam">`   | Chọn 1 trong nhiều lựa chọn |
| `checkbox` | `<input type="checkbox" name="sothich" value="web">` | Chọn nhiều giá trị          |
| `submit`   | `<input type="submit" value="Gửi">`                  | Nút gửi form                |
| `reset`    | `<input type="reset" value="Xóa hết">`               | Xóa toàn bộ dữ liệu         |

```html
<h2>Form đăng ký</h2>

<form action="dangky.php" method="POST">
  <label for="hoten">Họ tên:</label><br>
  <input type="text" id="hoten" name="hoten"><br><br>

  <label for="email">Email:</label><br>
  <input type="email" id="email" name="email"><br><br>

  <label>Giới tính:</label><br>
  <input type="radio" name="gioitinh" value="Nam"> Nam
  <input type="radio" name="gioitinh" value="Nữ"> Nữ<br><br>

  <label>Sở thích:</label><br>
  <input type="checkbox" name="sothich" value="Web"> Web
  <input type="checkbox" name="sothich" value="Game"> Game
  <input type="checkbox" name="sothich" value="Đọc sách"> Đọc sách<br><br>

  <label for="ghichu">Ghi chú:</label><br>
  <textarea id="ghichu" name="ghichu" rows="4" cols="40"></textarea><br><br>

  <input type="submit" value="Đăng ký">
  <input type="reset" value="Nhập lại">
</form>
```

## Thẻ ngữ nghĩa

---
- Hiểu được tầm quan trọng của thẻ ngữ nghĩa trong `HTML5`
- Biết cách sử dụng các thẻ `semantic` như: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, v.v.
- So sánh thẻ `semantic` với `<div>` thông thường


`Semantic` tags là các thẻ `HTML` có ý nghĩa rõ ràng về nội dung và vai trò trong cấu trúc trang `web`.
|  Không semantic     |  Semantic tương đương  |
| ------------------- | ---------------------- |
| `<div id="header">` | `<header>`             |
| `<div id="menu">`   | `<nav>`                |
| `<div id="footer">` | `<footer>`             |
> - Tăng khả năng đọc hiểu của trình duyệt & máy tìm kiếm (Google, Bing...)
> - Bố cục rõ ràng, dễ bảo trì

### Các thẻ ngữ nghĩa phổ biến
| Thẻ         | Ý nghĩa          | Mục đích sử dụng                  |
| ----------- | ---------------- | --------------------------------- |
| `<header>`  | Phần đầu trang   | Chứa logo, tiêu đề, menu          |
| `<nav>`     | Điều hướng       | Chứa các liên kết chuyển trang    |
| `<main>`    | Nội dung chính   | Nội dung trung tâm của trang      |
| `<section>` | Khu vực nội dung | Nhóm các nội dung có liên quan    |
| `<article>` | Bài viết độc lập | Blog, tin tức, bài đăng           |
| `<aside>`   | Bên lề           | Quảng cáo, thông tin phụ          |
| `<footer>`  | Chân trang       | Chứa thông tin bản quyền, liên hệ |
