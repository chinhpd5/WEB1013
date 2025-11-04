# Các thẻ HTML cơ bản

Mục tiêu buổi học:
- Tìm hiểu với các thẻ (`tag`) cơ bản
- Biết cách sử dụng các thẻ (`tag`)

## HTML Headings - Tiêu đề
- Tiêu đề HTML là tiêu đề hoặc phụ đề mà bạn muốn hiển thị trên trang web.
- Tiêu đề HTML được định nghĩa bằng thẻ `<h1>` đến `<h6>`
- `<h1>` định nghĩa tiêu đề quan trọng nhất. `<h6>` định nghĩa tiêu đề ít quan trọng nhất.

Ví dụ:
```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

## HTML Paragraphs - Đoạn văn bản
- Phần tử HTML `<p>` định nghĩa một đoạn văn.
- Một đoạn văn luôn bắt đầu ở một dòng mới và trình duyệt sẽ tự động thêm một khoảng trắng (lề) trước và sau một đoạn văn.

```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
<p>
This paragraph
contains a lot of lines
in the source code,
but the browser
ignores it.
</p>
```
> Sử dụng thẻ `<br>` để xuống dòng
> Hoặc sử dụng thẻ `<pre></pre>` để giữ nguyên định dạng

## HTML Formatting - Thẻ định dạng

| **Thẻ**    | **Chức năng / Ý nghĩa**                    | **Ví dụ hiển thị**              |
| ---------- | ------------------------------------------ | ------------------------------- |
| `<b>`      | In đậm (bold) – **trang trí**              | **Đây là chữ đậm**              |
| `<strong>` | In đậm – **nhấn mạnh nội dung quan trọng** | **Đây là nội dung quan trọng**  |
| `<i>`      | In nghiêng (italic) – **trang trí**        | *Đây là chữ nghiêng*            |
| `<em>`     | In nghiêng – **nhấn mạnh nhẹ**             | *Đây là nội dung cần nhấn mạnh* |
| `<mark>`   | **Tô sáng nội dung**                       | <mark>Chữ được đánh dấu</mark>  |
| `<small>`  | Văn bản nhỏ hơn bình thường                | <small>Chữ nhỏ</small>          |
| `<del>`    | Gạch ngang chữ – nội dung bị xóa           | <del>Giá cũ: 500.000đ</del>     |
| `<ins>`    | Gạch dưới – nội dung được chèn vào         | <ins>Giá mới: 450.000đ</ins>    |
| `<sub>`    | Chỉ số dưới (subscript)                    | H<sub>2</sub>O                  |
| `<sup>`    | Chỉ số trên (superscript)                  | X<sup>2</sup> + Y<sup>2</sup>   |

> Nên ưu tiên dùng <strong> và <em> thay cho <b>, <i> để đảm bảo ngữ nghĩa rõ ràng, tốt cho SEO và trợ năng (Accessibility).
> Các thẻ này thuộc nhóm inline elements – không tự tạo dòng mới.

## HTML Links - Thẻ liên kết
- Có thể nhấp vào liên kết và chuyển đến tài liệu khác.
- Khi  di chuyển chuột qua một liên kết, mũi tên chuột sẽ biến thành hình bàn tay nhỏ.
```html
<a href="url">link text</a>
```
> Thuộc tính quan trọng nhất của <a> phần tử là `href` thuộc tính cho biết đích đến của liên kết.

| `target` | **Chức năng**                                           | **Ví dụ minh họa**                                            |
| -------- | ------------------------------------------------------- | ------------------------------------------------------------- |
| `_self`  | **Mặc định** – Mở liên kết trong **chính tab hiện tại** | `<a href="about.html" target="_self">Giới thiệu</a>`          |
| `_blank` | Mở liên kết trong **tab hoặc cửa sổ mới**               | `<a href="https://fpt.edu.vn" target="_blank">Website FPT</a>`|
| `_parent`| Mở trong **khung cha (frame/iframe)** nếu có            | `<a href="frame.html" target="_parent">Mở trong khung cha</a>`|
| `_top`   | Mở trong **toàn bộ cửa sổ**, loại bỏ mọi khung lồng nhau| `<a href="main.html" target="_top">Mở toàn màn hình</a>`      |

## HTML Images - thẻ hình ảnh
Thẻ dùng để tạo hình ảnh trên `website`:
Ví dụ:
```html
<img src="image.jpg" alt="Description">
<img src="https://source/image.jpg" alt="Description">
```

> <img> trống, chỉ chứa các thuộc tính và không có thẻ đóng.
> <img> có hai thuộc tính bắt buộc:
>   + `src` - Chỉ định đường dẫn đến hình ảnh
>   + `alt` - Chỉ định văn bản thay thế cho hình ảnh

## HTML Lists - Thẻ danh sách
Dùng để thể hiện danh sách
Ví dụ:
```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```
> `ul` không đánh số thứ tự
> `ol` đánh số thứ tự: `type="1"` -> 1, 2, 3, ...
> `ol` đánh số thứ tự: `type="A"` -> A, B, C, ...
> `ol` đánh số thứ tự: `type="a"` -> a, b, c, ...
> `ol` đánh số thứ tự: `type="I"` -> I, II, III, ...
> `ol` đánh số thứ tự: `type="i"` -> i, ii, iii, ...

