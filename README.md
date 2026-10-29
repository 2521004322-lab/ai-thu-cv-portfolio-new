# Website CV — Hồ Phạm Ái Thư

Website tĩnh dùng HTML, CSS và JavaScript thuần. Có thể deploy trực tiếp bằng Netlify từ repository GitHub, không cần build command hay backend.

## Cấu trúc thư mục

```text
ai-thu-cv/
├── index.html
├── styles.css
├── script.js
├── README.md
└── assets/
    ├── avatar-placeholder.svg
    └── cv.pdf
```

## Thay ảnh chân dung

1. Chuẩn bị ảnh chân dung, nên dùng ảnh dọc, rõ mặt.
2. Đặt ảnh vào thư mục `assets/` và đặt tên `avatar.jpg`.
3. Trong `index.html`, tìm:
   ```html
   <img id="profilePhoto" src="assets/avatar-placeholder.svg" data-placeholder="assets/avatar-placeholder.svg" alt="Ảnh đại diện của Hồ Phạm Ái Thư">
   ```
4. Đổi `src="assets/avatar-placeholder.svg"` thành `src="assets/avatar.jpg"`.
5. Giữ nguyên `data-placeholder` để website có ảnh dự phòng nếu ảnh không tải được.
6. Upload ảnh lên GitHub cùng các file khác. Tên file và chữ hoa/chữ thường phải khớp chính xác.

## Thay hoặc cập nhật CV PDF

File `assets/cv.pdf` là bản CV PDF được tạo từ thông tin hiện có. Để thay bằng bản PDF mới, xuất CV của bạn thành PDF, đặt tên chính xác là `cv.pdf` rồi ghi đè file trong thư mục `assets/`.

## Đăng lên GitHub

1. Tạo repository mới trên GitHub, ví dụ `ai-thu-cv`.
2. Upload toàn bộ nội dung trong thư mục `ai-thu-cv` vào thư mục gốc của repository (không chỉ upload file ZIP).
3. Kiểm tra `index.html` nằm ngay ở root của repository, không nằm sâu trong một thư mục con.
4. Commit changes.

## Kết nối GitHub với Netlify

1. Đăng nhập hoặc tạo tài khoản tại https://app.netlify.com/.
2. Chọn **Add new site** → **Import an existing project**.
3. Chọn **GitHub**, cấp quyền cho Netlify truy cập repository `ai-thu-cv`.
4. Chọn repository vừa tạo.
5. Vì đây là website HTML/CSS/JS thuần, để trống **Build command** và đặt **Publish directory** là `.` (dấu chấm, thư mục gốc).
6. Chọn **Deploy site**.
7. Sau khi deploy xong, Netlify sẽ cấp một URL dạng `https://ten-ngau-nhien.netlify.app`. Bạn có thể đổi tên site trong phần **Site configuration / Site details** nếu tên mong muốn còn trống.

Khi cập nhật code rồi push/commit lên branch đã kết nối, Netlify sẽ tự deploy lại.

## Lưu ý về nội dung

- Các mức kỹ năng hiển thị trên website là mức tự đánh giá minh họa, chưa được xác nhận bởi bài kiểm tra. Hãy sửa các phần trăm trong `index.html` nếu muốn phản ánh đúng năng lực.
- Thông tin liên hệ được đưa lên website công khai. Chỉ giữ số điện thoại và email nếu bạn đồng ý công khai chúng.
- Website không cần API key, backend hoặc biến môi trường.
