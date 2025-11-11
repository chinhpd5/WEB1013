# Những thuộc tính cơ bản trong CSS

Mục tiêu buổi học:
- Hiểu `CSS` là gì, hoạt động như thế nào
- Biết 3 cách nhúng `CSS` vào `HTML`: `Inline`, `Internal`, `External`
- Viết được cú pháp `CSS` cơ bản
- Bắt đầu định dạng chữ, màu sắc, căn lề cơ bản cho website

## CSS là gì ?
`Cascading Style Sheets` là ngôn ngữ tạo phong cách cho các tài liệu `HTML`.
`CSS` giúp bạn trang trí giao diện web: thay đổi màu sắc, font chữ, kích thước, khoảng cách, vị trí, hiệu ứng, bố cục...
> Nói đơn giản: `HTML` là “bộ xương”, còn `CSS` là “da, tóc, quần áo” của một `website`.


## Cú pháp CSS cơ bản

```css
h1 {
  color: blue;
  font-size: 32px;
}
```
> thẻ `h1` → đổi màu → đổi kích thước chữ


## Cách viết
| Cách viết      | Cú pháp ví dụ                                           | Ưu – Nhược điểm                         |
| -------------- | ------------------------------------------------------- | --------------------------------------- |
| Inline CSS     | `<p style="color: red;">Text</p>`                       | Nhanh, đơn giản – **nhưng khó bảo trì** |
| Internal CSS   | Viết trong thẻ `<style>` trong `<head>`                 | Tốt khi trang nhỏ                       |
| External CSS   | Viết CSS trong file `.css` và dùng `<link>` để liên kết | **Tốt nhất**, dễ tái sử dụng            |

Ví dụ về `Internal`
```html
<head>
  <style>
    body {
      background-color: #f0f0f0;
      font-family: Arial;
    }
    h1 {
      color: green;
    }
  </style>
</head>
```

Ví dụ về `External`
Tạo `style.css` và sử dụng thẻ `<link rel="stylesheet" href="style.css">` bên trong thẻ `<head></head>`
```css
/* style.css */
h1 {
  color: navy;
}
p {
  font-size: 18px;
}
```
> `/* style.css */` là comment trong `css`

## Các css cơ bản làm việc với chữ

| **Thuộc tính**    | **Chức năng**                              | **Ví dụ**                     |
| ----------------- | ------------------------------------------ | ----------------------------- |
| `color`           | Màu chữ                                    | `color: red;`                 |
| `background-color`| Màu nền chữ                                | `background-color: blue;`     |
| `font-size`       | Kích thước chữ                             | `font-size: 20px;`            |
| `font-family`     | Kiểu font chữ                              | `font-family: Arial;`         |
| `font-weight`     | Độ đậm của chữ                             | `font-weight: bold;`          |
| `font-style`      | Kiểu nghiêng (italic)                      | `font-style: italic;`         |
| `text-align`      | Căn lề: left, right, center, justify       | `text-align: center;`         |
| `text-decoration` | Trang trí chữ (gạch chân, gạch ngang…)     | `text-decoration: underline;` |
| `text-transform`  | Viết hoa, thường, in hoa mỗi từ            | `text-transform: uppercase;`  |
| `line-height`     | Khoảng cách giữa các dòng                  | `line-height: 1.5;`           |
| `letter-spacing`  | Khoảng cách giữa các chữ cái               | `letter-spacing: 2px;`        |
| `word-spacing`    | Khoảng cách giữa các từ                    | `word-spacing: 5px;`          |

