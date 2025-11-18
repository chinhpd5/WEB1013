# Căn giữa và Thuộc tính Display trong CSS

Mục tiêu buổi học:
- Nắm rõ các cách căn giữa nội dung theo chiều ngang, chiều dọc, và cả hai
- Hiểu rõ các giá trị phổ biến của `display` và cách ảnh hưởng đến bố cục trang web
- Ứng dụng vào thiết kế giao diện web đơn giản

---
## Cách căn giữa theo chiều ngang
1. Căn giữa khối (block)
Áp dụng khi phần tử có `width` cố định:
```css
.box {
  width: 300px;
  margin: 0 auto;
}
```
> `margin: 0 auto` chỉ hoạt động nếu phần tử có `width` xác định và `display: block` hoặc `inline-block`

2. Căn giữa chữ (inline text)
```css
.text-container {
  text-align: center;
}
```

## Cách căn giữa theo chiều dọc
1. Căn giữa trong khối có chiều cao cố định
```css
.wrapper {
  height: 300px;
  line-height: 300px; /* Dòng cao bằng chiều cao */
  text-align: center;
}
```

2. Căn giữa bằng position + transform
```css
.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

## Căn giữa bằng display: flex
1. `Flexbox` là gì?
`Flexbox` (Flexible Box) là một mô hình bố cục CSS dùng để sắp xếp các phần tử một cách linh hoạt và dễ kiểm soát hơn trong một `container`.
Giải quyết rất tốt các bài toán:
- Căn giữa phần tử (theo mọi hướng)
- Chia `layout` hàng ngang / cột dọc
- Co giãn linh hoạt các phần tử trong `layout`

2. Cấu trúc Flexbox
| Thành phần         | Mô tả                                      |
| ------------------ | ------------------------------------------ |
| **Flex Container** | Phần tử cha – nơi khai báo `display: flex` |
| **Flex Items**     | Các phần tử con bên trong container        |

3. Cách sử dụng
```css
.container {
  display: flex;
}
```

4. Các thuộc tính quan trọng
| Thuộc tính        | Ý nghĩa                                                 |
| ----------------- | ------------------------------------------------------- |
| `display: flex`   | Biến phần tử thành Flex Container                       |
| `flex-direction`  | Xác định **hướng chính**: `row` (ngang), `column` (dọc) |
| `justify-content` | Căn chỉnh các item **theo trục chính**                  |
| `align-items`     | Căn chỉnh item **theo trục phụ** (vuông góc trục chính) |
| `flex-wrap`       | Cho phép các item **xuống dòng** nếu quá dài            |
| `gap`             | Khoảng cách giữa các item (CSS3 mới, thay `margin`)     |

Ví dụ:
```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}
```