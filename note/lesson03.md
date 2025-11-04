# Các thẻ Nâng cao - Thẻ ngữ nghĩa

Mục tiêu bài học:
- Tìm hiểu và thực hành các thẻ `table`, `form`
- Tìm hiểu các thẻ ngữ nghĩa

## HTML Tables - Thẻ tạo bảng
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