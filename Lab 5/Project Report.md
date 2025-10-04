# Gom tất cả artifacts (các sản phẩm trước)
| Hạng mục         | Tệp hoặc ảnh                   | Ghi chú                         |
| ---------------- | ------------------------------ | ------------------------------- |
| Use Case Diagram | `UseCaseDiagram.png`           | Vẽ bằng PlantUML hoặc Draw.io   |
| Sequence Diagram | `SequenceDiagram.png`          | Luồng “Đặt phòng và Thanh toán” |
| Form Login       | `index.html`                   | Code đã làm ở Lab 04            |
| Báo cáo          | `ProjectReport.pdf` hoặc `.md` | Mô tả toàn bộ quy trình         |
# Quy trình làm việc
– Hệ thống quản lý đặt phòng khách sạn
1. Giới thiệu hệ thống
- Hệ thống giúp khách hàng có thể:
- Tìm kiếm và đặt phòng khách sạn.
- Thanh toán trực tuyến.
- Quản lý thông tin đặt phòng.
2. Phân tích yêu cầu & Use Case
# Các tác nhân:
- Khách hàng
- Hệ thống quản lý khách sạn
- Cổng thanh toán (Payment Gateway)
## Use Case chính:
- Đăng ký / Đăng nhập
- Tìm kiếm phòng
- Đặt phòng
- Thanh toán
- Hủy phòng
- Hình: UCdiagramlab02.png
3. Thiết kế tương tác (Sequence Diagram)
- Luồng “Đặt phòng và Thanh toán”:
- Khách hàng chọn phòng.
- Hệ thống hiển thị thông tin phòng.
- Khách hàng xác nhận đặt phòng.
- Hệ thống gửi yêu cầu thanh toán đến cổng Payment.
- Payment phản hồi kết quả giao dịch.
- Hệ thống cập nhật trạng thái đặt phòng.
- Hình: sqdlab3.png
4. Giao diện người dùng (Front-end)
- Giao diện đăng nhập: code form login.html
- Gồm input Email, nút Đăng nhập bằng Google/Facebook/Apple, nút Tiếp tục.
- Dùng HTML + CSS + JavaScript..
# Cách push lên GitHub:
# 1. Tạo repo mới
git init
git remote add origin https://github.com/<tên_user>/HotelBookingSystem.git
# 2. Thêm file
git add .
git commit -m "Add Use Case, Sequence, and Login form"
# 3. Push lần đầu
git branch -M main
git push -u origin main
# 4. Tạo tag version v1.0
git tag v1.0
git push origin v1.0
