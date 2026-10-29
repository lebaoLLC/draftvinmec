# MyVinmec: bản nền (backup) để khảo sát và phỏng vấn khách

Website tĩnh đã build sẵn, không cần cài đặt gì. Đây là bản xuất phát, chưa có phần cá nhân hóa theo từng người dùng.

## Bản này có gì
- Mở app là vào luôn, không đăng nhập. Người dùng là một bệnh nhân mẫu (Bà Phạm Thị Thu Hà, 47 tuổi, sau phẫu thuật thay khớp gối) với đơn thuốc mẫu.
- Nhắc uống thuốc, kế hoạch phục hồi, bài tập và video hướng dẫn cho chấn thương chân (một video: `video/tri-lieu-phuc-hoi.mp4`).
- Thêm người thân, đặt lịch hẹn có chọn bác sĩ, tư vấn từ xa, theo dõi nội trú và các màn hình dịch vụ khác của app.
- Lời nhắc thuốc đọc bằng giọng đọc của trình duyệt (cần máy có giọng tiếng Việt), gọi tên bệnh nhân mẫu.

## Bản này chưa có (để hỏi khách)
- Đăng nhập theo từng người, mỗi người một hồ sơ, thuốc và người thân riêng.
- Tải hồ sơ bệnh án và đơn thuốc để app tự nhận diện chấn thương và tự lập lịch uống thuốc.
- Cá nhân hóa theo loại chấn thương (tay, chân) và video bài tập cho chấn thương tay.
- Chia sẻ lịch cho người thân bằng liên kết gửi qua tin nhắn hoặc email, lời nhắc thuốc đọc trung tính cho mọi người dùng.

## Đăng bằng GitHub Pages
1. Tạo repo mới trên GitHub, upload toàn bộ file trong thư mục này (kể cả file ẩn `.nojekyll`). Thư mục có dưới 100 file nên kéo thả một lần được; video nặng khoảng 14 MB, dưới giới hạn 25 MB của upload qua web.
2. Vào Settings > Pages > Build and deployment, Source chọn "Deploy from a branch", Branch chọn `main` và thư mục `/ (root)`, bấm Save.
3. Chờ 1 đến 2 phút, địa chỉ hiện ở đầu trang Pages: https://TEN-USER.github.io/TEN-REPO/

Nếu dùng git thay vì kéo thả:

```bash
git init -b main
git add -A
git commit -m "MyVinmec ban nen"
git remote add origin https://github.com/TEN-USER/TEN-REPO.git
git push -u origin main
```

## Xem thử trên máy
Mở bằng một server tĩnh bất kỳ, ví dụ `npx serve` trong thư mục này. Mở trực tiếp file `index.html` bằng đường dẫn `file://` sẽ không chạy vì trình duyệt chặn module.

## Ghi chú
- Dữ liệu lưu trong trình duyệt (localStorage), không có máy chủ.
- Đây là bản thiết kế, không liên kết với Vinmec.
- Ảnh bác sĩ và các ảnh minh hoạ được cắt từ ảnh tham chiếu của tác giả, chỉ mang tính minh hoạ. Hãy thay bằng ảnh có bản quyền phù hợp trước khi công khai.
