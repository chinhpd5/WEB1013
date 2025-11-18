# Position trong CSS

Mục tiêu buổi học
- Hiểu rõ các giá trị của thuộc tính position
- Biết cách định vị phần tử theo tọa độ: top, left, right, bottom
- Phân biệt giữa các loại position: static, relative, absolute, fixed, sticky
- Ứng dụng trong thiết kế layout và hiệu ứng đơn giản

## position là gì?

`position` là thuộc tính `CSS` giúp xác định cách trình duyệt sắp xếp phần tử trong trang web. Khi sử dụng, bạn có thể kết hợp với `top`, `left`, `right`, `bottom` để định vị chính xác.

## Các giá trị của position

1. `static` (mặc định):
- Phần tử nằm theo luồng thông thường của tài liệu
- Không thể dùng `top`, `left`, `right`, `bottom`
```css
div {
  position: static;
}
```
2. `relative` (tương đối)
- Phần tử vẫn giữ chỗ cũ, nhưng có thể dịch chuyển so với vị trí ban đầu
- Dùng được các thuộc tính định vị
```css
.box {
  position: relative;
  top: 10px;
  left: 20px;
}
```

3. `absolute` (tuyệt đối)
- Phần tử bỏ ra khỏi luồng thông thường
- Được định vị so với phần tử cha gần nhất có `position`: `relative` hoặc `absolute`
- Nếu không có cha định vị → định vị theo `<body>`
```css
.box {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

4. `fixed` (cố định)
- Phần tử cố định theo cửa sổ trình duyệt, không cuộn theo trang
- Rất hay dùng cho: nút quay về đầu trang, menu `sticky`...
```css
.fixed-menu {
  position: fixed;
  top: 0;
  right: 0;
}
```

5. `sticky` (dính)
- Kết hợp `relative` + `fixed`
- Cuộn đến vị trí thì “dính lại”, cuộn lên thì trở lại bình thường
- Hay dùng cho tiêu đề bảng, thanh điều hướng
```css
.sticky {
  position: sticky;
  top: 0;
}
```

## So sánh nhanh
| Thuộc tính | Theo luồng tài liệu? | Định vị theo gì?                   | Di chuyển được? |
| ---------- | -------------------- | ---------------------------------- | --------------- |
| `static`   |  Có                  | Không định vị                      |  Không          |
| `relative` |  Có                  | Vị trí ban đầu của chính nó        |  Có             |
| `absolute` |  Không               | Phần tử cha gần nhất có `position` |  Có             |
| `fixed`    |  Không               | Cửa sổ trình duyệt                 |  Có             |
| `sticky`   |  Có                  | Cuộn tới vị trí sẽ dính lại        |  Có             |
