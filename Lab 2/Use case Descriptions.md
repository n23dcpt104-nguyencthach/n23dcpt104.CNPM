# Viết Use Case Description (2 chức năng quan trọng)
## Use Case 1: Đặt phòng
| Thành phần               | Mô tả                                                                                                                                                        |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Tên Use Case**         | Đặt phòng                                                                                                                                                    |
| **Tác nhân chính**       | Khách hàng                                                                                                                                                   |
| **Mục tiêu**             | Cho phép khách hàng đặt phòng khách sạn theo ngày và loại phòng mong muốn.                                                                                   |
| **Điều kiện tiên quyết** | Khách hàng đã đăng nhập vào hệ thống.                                                                                                                        |
| **Mô tả tóm tắt**        | Khách hàng chọn phòng, nhập thông tin thời gian lưu trú, xác nhận và lưu đặt phòng.                                                                          |
| **Luồng chính**          | 1. Khách hàng tìm kiếm phòng trống.<br>2. Chọn loại phòng.<br>3. Nhập ngày nhận/trả phòng.<br>4. Xác nhận đặt phòng.<br>5. Hệ thống lưu thông tin đặt phòng. |
| **Luồng phụ (nếu có)**   | Nếu phòng đã được đặt, hệ thống thông báo và yêu cầu chọn phòng khác.                                                                                        |
| **Kết quả**              | Thông tin đặt phòng được lưu và gửi xác nhận.                                                                                                                |

## Use Case 2: Thanh toán đặt phòng
| Thành phần               | Mô tả                                                                                                                                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Tên Use Case**         | Thanh toán đặt phòng                                                                                                                                                                       |
| **Tác nhân chính**       | Khách hàng                                                                                                                                                                                 |
| **Mục tiêu**             | Khách hàng hoàn tất thanh toán cho đơn đặt phòng.                                                                                                                                          |
| **Điều kiện tiên quyết** | Đã có đơn đặt phòng hợp lệ.                                                                                                                                                                |
| **Mô tả tóm tắt**        | Khách hàng chọn phương thức thanh toán và xác nhận.                                                                                                                                        |
| **Luồng chính**          | 1. Khách hàng chọn đơn đặt phòng chưa thanh toán.<br>2. Chọn phương thức thanh toán (ví điện tử, thẻ, tiền mặt, v.v.).<br>3. Xác nhận thanh toán.<br>4. Hệ thống ghi nhận và gửi biên lai. |
| **Luồng phụ**            | Nếu thanh toán thất bại, hệ thống hiển thị thông báo lỗi và yêu cầu thử lại.                                                                                                               |
| **Kết quả**              | Thanh toán thành công, phòng được giữ chỗ.                                                                                                                                                 |
