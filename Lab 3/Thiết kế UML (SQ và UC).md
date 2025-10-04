# Mô tả luồng tương tác chi tiết

| **Bước** | **Mô tả hành động**                                                                  | **Đối tượng tham gia**         |
| :------: | :----------------------------------------------------------------------------------- | :----------------------------- |
|     1    | Khách hàng đăng nhập vào hệ thống bằng tài khoản đã có.                              | Customer → HotelSite → HotelDB |
|     2    | Hệ thống xác thực thông tin đăng nhập, cho phép truy cập nếu hợp lệ.                 | HotelDB                        |
|     3    | Khách hàng nhập thông tin tìm kiếm (ngày đến, ngày đi, loại phòng).                  | Customer                       |
|     4    | Hệ thống truy vấn CSDL để lấy danh sách phòng trống.                                 | HotelSite → HotelDB            |
|     5    | Khách hàng chọn phòng muốn đặt và nhập thông tin cá nhân.                            | Customer                       |
|     6    | Hệ thống lưu thông tin đặt phòng tạm thời vào CSDL.                                  | HotelSite → HotelDB            |
|     7    | Khách hàng xác nhận thanh toán.                                                      | Customer                       |
|     8    | Hệ thống gửi yêu cầu thanh toán đến cổng thanh toán (Payment Gateway).               | HotelSite → PaymentGateway     |
|     9    | Cổng thanh toán xác thực thẻ, xử lý giao dịch và trả kết quả.                        | PaymentGateway → HotelSite     |
|    10    | Nếu thanh toán thành công, hệ thống cập nhật trạng thái đặt phòng = “Đã thanh toán”. | HotelSite → HotelDB            |
|    11    | Hệ thống hiển thị thông báo “Đặt phòng thành công” cùng mã đơn.                      | HotelSite → Customer           |
|    12    | Nếu thanh toán thất bại, hệ thống thông báo lỗi và cho phép thử lại.                 | HotelSite → Customer           |

## Luồng phụ (Alternative Flow)
| **Tình huống**                  | **Xử lý**                                                                |
| ------------------------------- | ------------------------------------------------------------------------ |
| **Sai tài khoản hoặc mật khẩu** | Hệ thống báo lỗi đăng nhập, yêu cầu nhập lại.                            |
| **Không có phòng trống**        | Hiển thị thông báo “Không còn phòng phù hợp với yêu cầu”.                |
| **Thanh toán thất bại**         | Hiển thị “Giao dịch thất bại, vui lòng thử lại” và giữ đơn đặt tạm thời. |
| **Cổng thanh toán mất kết nối** | Thông báo “Lỗi hệ thống thanh toán”, tạm dừng quy trình.                 |
## Giải thích đối tượng và thông điệp trao đổi
| **Đối tượng**                        | **Vai trò**                                                 | **Thông điệp chính**                                                      |
| ------------------------------------ | ----------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Khách hàng (Customer)**            | Tác nhân chính, khởi tạo và điều khiển quy trình đặt phòng. | Gửi yêu cầu đăng nhập, tìm phòng, đặt phòng, thanh toán.                  |
| **Website khách sạn (HotelSite)**    | Giao diện trung gian giữa khách hàng và hệ thống.           | Hiển thị thông tin, xử lý yêu cầu, giao tiếp với CSDL và cổng thanh toán. |
| **CSDL khách sạn (HotelDB)**         | Nơi lưu trữ thông tin phòng, đặt phòng, khách hàng.         | Xác thực, truy vấn và cập nhật dữ liệu.                                   |
| **Cổng thanh toán (PaymentGateway)** | Dịch vụ xử lý giao dịch tài chính.                          | Nhận yêu cầu thanh toán, xác nhận kết quả giao dịch.                      |
