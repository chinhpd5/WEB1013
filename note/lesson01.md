# Buổi 1: GIỚI THIỆU MÔN HỌC & HTML CƠ BẢN

Mục tiêu:
1. Hiểu khái niệm website, cách website hoạt động trên Internet.
2. Biết tạo một file HTML đầu tiên và hiển thị nội dung trên trình duyệt.
3. Nắm được cấu trúc cơ bản của tài liệu HTML.
4. Biết sử dụng các thẻ văn bản cơ bản như: `<h1>`, `<p>`, `<br>`, `<strong>`, `<em>`

## Website là gì?
- `Website`: tập hợp các trang web `(web pages)` liên kết với nhau.
- `Webpage`: một tệp tin HTML được hiển thị trên trình duyệt (Chrome, Edge…).
- `HTML` `(HyperText Markup Language)` là ngôn ngữ đánh dấu dùng để tạo cấu trúc cho trang web.
- `CSS` `(Cascading Style Sheets)` dùng để định dạng, làm đẹp trang web.
- `Browser` (Trình duyệt) là phần mềm giúp hiển thị `website`.
Ví dụ: Khi truy cập https://fpt.edu.vn, trình duyệt gửi yêu cầu đến máy chủ của FPT, nhận file `HTML` và hiển thị nội dung.

## Khái niệm
### HTML
`HyperText Markup Language` là ngôn ngữ đánh dấu siêu văn bản, được dùng để xây dựng cấu trúc và nội dung cho trang web.
Nói cách khác, `HTML` là “bộ khung xương” của `website` — giúp trình duyệt hiểu và hiển thị nội dung như:
> Tiêu đề, đoạn văn, hình ảnh, liên kết, bảng, form, video, v.v.
>  - `“HyperText”` nghĩa là văn bản có chứa liên kết (`link`) đến tài nguyên khác.
>  - “Markup Language” nghĩa là ngôn ngữ dùng các thẻ (`tags`) để đánh dấu và mô tả nội dung.

Ví dụ:
```html
<h1>Giới thiệu bản thân</h1>
<p>Xin chào! Tôi là <strong>Nguyễn Văn A</strong>.</p>
<p>Tôi đang học môn <em>Xây dựng trang web</em> tại FPT Polytechnic.</p>
```
> 

### CSS
`Cascading Style Sheets` là ngôn ngữ tạo phong cách cho các tài liệu `HTML`.
`CSS` giúp bạn trang trí giao diện web: thay đổi màu sắc, font chữ, kích thước, khoảng cách, vị trí, hiệu ứng, bố cục...

> Nói đơn giản: `HTML` là “bộ xương”, còn `CSS` là “da, tóc, quần áo” của một `website`.

```css
h1 {
  color: red;
  font-size: 36px;
}
```
## Làm việc HTML
- Tạo 1 `file` trong `lesson01`: `lesson01/index.html` và thêm nội dung:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trang đầu tiên của tôi</title>
  </head>
  <body>
    <h1>Hello world!</h1>
    <p>Đây là trang web đầu tiên của tôi.</p>
  </body>
</html>
```
- Sử dụng `Live Server` để chạy dự án

### Giải thích:
1. `<!DOCTYPE html>`
 - Mục đích: Khai báo tài liệu sử dụng chuẩn `HTML5`.
 - Ý nghĩa: Giúp trình duyệt hiểu đúng cách phân tích cú pháp và hiển thị trang web.
 - Đây không phải là thẻ `HTML`, chỉ là một dòng khai báo đặc biệt ở đầu tài liệu.

2. `<html lang="en">`
- Thẻ mở đầu của toàn bộ tài liệu `HTML`.
- Bao trùm toàn bộ nội dung trên trang web.
- Thuộc tính `lang="en"`:
  + Chỉ định ngôn ngữ sử dụng là tiếng Anh.
  + Tốt cho `SEO` và hỗ trợ công cụ đọc màn hình (screen reader).

3. `<head>`
- Phần đầu trang chứa các thông tin cấu hình, không hiển thị ra màn hình.
- Thường bao gồm:
  + Tiêu đề trang (`<title>`)
  + Khai báo mã hóa (`<meta charset>`)
  + Khai báo responsive (`<meta viewport>`)
  + `Link CSS`, `favicon`, `script` v.v.

3.1 `<meta charset="UTF-8">`
- Khai báo bảng mã ký tự dùng trong trang web là `UTF-8`.
- `UTF-8` hỗ trợ đầy đủ tiếng Việt, emoji, ký tự đặc biệt…
- Nếu không khai báo, có thể bị lỗi hiển thị dấu tiếng Việt.

3.2 `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Giúp `website` hiển thị tốt trên thiết bị di động (responsive).
- Giải thích:
  + `width=device-width`: Chiều rộng trang web bằng chiều rộng thiết bị.
  + `initial-scale=1.0`: Tỷ lệ zoom ban đầu là 100%

3.3 `<title>Trang đầu tiên của tôi</title>`
- Hiển thị trên thẻ tiêu đề (tab) của trình duyệt.
- Cũng là nội dung được hiển thị khi người dùng `bookmark` trang web.

4. `<body>`
- Phần nội dung chính của trang web — tất cả những gì người dùng nhìn thấy.
- Trong ví dụ này, phần `<body>` chứa:

4.1 `<h1>Hello world!</h1>`
- Thẻ tiêu đề lớn nhất, thường dùng cho tiêu đề chính của trang.

4.2 `<p>Đây là trang web đầu tiên của tôi.</p>`
- Thẻ đoạn văn bản (`paragraph`).
- Dùng để trình bày nội dung chính dưới dạng đoạn.

## HTML Elements - Phần tử
- Phần tử HTML bao gồm mọi thứ từ thẻ bắt đầu đến thẻ kết thúc: `<tagname> Nội dung sẽ ở đây ... </tagname>`
- Nội dung ở giữa thẻ mở và đóng sẽ hiển thị ra giao diện
- Ví dụ về một số phần tử HTML:
```html
<h1>My First Heading</h1>
<p>My first paragraph.</p>
<br>
```
> img là 1 thẻ đặc biệt có thể chỉ có thẻ mở và không có thẻ đóng, dùng để hiển thị hình ảnh
> ngoài ra còn có 1 số thẻ khác: img, br, hr,...

## HTML Attributes - Thuộc tính
- Thuộc tính HTML cung cấp thông tin bổ sung về các thành phần HTML.
- Ví dụ:
```html
<h1 id="title" class="heading-1" style="color:red;">My First Heading</h1>
<a href="https://www.google.com">Google</a>
<img src="imgae.jpg" alt="Hình ảnh" width="500" height="600">
```

## Quy tắc viết HTML
- Mỗi thẻ có thẻ mở <tag> và thẻ đóng </tag>.
- Thẻ có thể lồng nhau, nhưng phải đóng đúng thứ tự.
→ Sai: `<p><strong>Xin chào!</p></strong>`
→ Đúng: `<p><strong>Xin chào!</strong></p>`
- Khoảng trắng không ảnh hưởng đến hiển thị.
- HTML không phân biệt chữ hoa/thường, nhưng nên viết thường.
- Comment `<!-- <h1>Heading</h1> -->`