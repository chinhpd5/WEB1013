# Box model, căn lề, định dạng viền khối

Mục tiêu buổi học:
- Hiểu và vẽ được mô hình `Box Model` trong `CSS`
- Biết cách sử dụng các thuộc tính: `margin`, `padding`, `border`, `width`, `height`
- Phân biệt các loại `display` cơ bản (`block`, `inline`, `inline-block`)
- Biết định dạng, căn lề và dãn khối nội dung

## CSS Box Model là gì?
`CSS` coi mọi phần tử trên `web` là một chiếc hộp. Mỗi hộp gồm 4 phần:
```lua
+--------------------------------+
|            margin              |
|  +--------------------------+  |
|  |         border           |  |
|  |  +--------------------+  |  |
|  |  |      padding       |  |  |
|  |  |  +--------------+  |  |  |
|  |  |  |   content    |  |  |  |
|  |  |  +--------------+  |  |  |
|  |  +--------------------+  |  |
|  +--------------------------+  |
+--------------------------------+
```
| Thành phần | Ý nghĩa                                                      |
| ---------- | ------------------------------------------------------------ |
| `content`  | Nội dung thực sự (chữ, ảnh,...)                              |
| `padding`  | Khoảng cách **bên trong**, giữa content và border            |
| `border`   | Đường viền bao quanh phần tử                                 |
| `margin`   | Khoảng cách **bên ngoài**, giữa phần tử này với phần tử khác |

## Các thuộc tính quan trọng
| Thuộc tính        | Chức năng                                   | Ví dụ                      |
| ----------------- | ------------------------------------------- | -------------------------- |
| `width`, `height` | Kích thước phần tử                          | `width: 300px;`            |
| `padding`         | Khoảng cách **bên trong**                   | `padding: 20px;`           |
| `margin`          | Khoảng cách **bên ngoài**                   | `margin: 10px auto;`       |
| `border`          | Viền xung quanh                             | `border: 1px solid black;` |
| `border-radius`   | Bo góc                                      | `border-radius: 8px;`      |
| `box-sizing`      | Kiểm soát kích thước tính cả padding/border | `box-sizing: border-box;`  |


## Thuộc tính display
| Giá trị        | Ý nghĩa                                           | Ứng dụng            |
| -------------- | ------------------------------------------------- | ------------------- |
| `block`        | Chiếm toàn bộ chiều ngang, tự xuống dòng          | `div`, `p`, `h1`... |
| `inline`       | Nằm trên cùng dòng, không set được `width/height` | `span`, `a`         |
| `inline-block` | Nằm cùng dòng nhưng vẫn set được `width/height`   | Khối nhỏ linh hoạt  |

Tạo 3 thẻ div có nội dung
```css
.block {
  width: 300px;
  height: 300px;
}

#div1 {
  background-color: red;
  display: block;
}

#div2 {
  background-color: blue;
  display: inline;
}

#div3 {
  background-color: green;
  display: inline-block;
}
```

## Bài tập:
```html
<div class="profile">
  <img src="https://via.placeholder.com/100" alt="avatar">
  <h2>Nguyễn Văn A</h2>
  <p>Web Developer</p>
</div>
```
Yêu cầu:
- Dùng 1 thẻ <div class="profile">
- Ảnh đại diện: dùng <img> (có bo tròn 50%)
Khối .profile có:
  - width: 300px, nền sáng
  - padding: 20px, viền bo tròn, căn giữa
  - box-sizing: border-box