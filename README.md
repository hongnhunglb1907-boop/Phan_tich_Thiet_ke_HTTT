### Hệ Thống Quản Lý Cửa Hàng Phụ Tùng Xe Máy Tài

> Dự án môn **Phân Tích & Thiết Kế HTTT** | Trường Đại Học Kinh Tế Đà Nẵng | 09/2025 - 12/2025

---

### Giới thiệu

**Cửa hàng phụ tùng xe máy Tài** (Thị trấn Di Lăng, Sơn Hà, Quảng Ngãi) đang vận hành toàn bộ hoạt động kinh doanh bằng sổ sách thủ công — dẫn đến sai sót trong tính toán tồn kho, khó kiểm soát nhập xuất hàng, và mất nhiều thời gian khi tra cứu thông tin.

Dự án tập trung vào việc:
- Thu thập và phân tích yêu cầu
- Xây dựng tài liệu SRS (Software Requirements Specification)
- Thiết kế hệ thống thông qua tài liệu SDS (Software Design Specification)
---

### Tính năng chính
### Đăng nhập & Tài khoản
- Đăng nhập bằng tên đăng nhập / mật khẩu
- Đặt lại mật khẩu qua xác thực OTP số điện thoại
- Đổi mật khẩu sau khi đăng nhập
- Đăng xuất an toàn, lưu dữ liệu chưa lưu

### Quản lý Nhập hàng
- Tạo, xem, chỉnh sửa hóa đơn nhập từ nhà cung cấp
- Tìm kiếm hóa đơn theo nhà cung cấp hoặc khoảng thời gian
- Tự động cập nhật số lượng tồn kho sau mỗi lần nhập

### Quản lý Bán hàng
- Tạo hóa đơn bán hàng, hỗ trợ in hóa đơn qua máy in USB
- Xem lịch sử giao dịch và chi tiết từng hóa đơn
- Quản lý đổi trả hàng: kiểm tra hợp lệ, tự động cập nhật tồn kho, tính chênh lệch giá

### Quản lý Hàng hóa
- Thêm, sửa, xem danh mục hàng hóa
- Quản lý giá bán theo thời gian, xem lịch sử thay đổi giá
- Cảnh báo tồn kho khi đạt mức tối thiểu / vượt mức tối đa
- Chiết khấu theo loại khách hàng (sỉ / lẻ)

### Quản lý Khách hàng & Công nợ
- Thêm, xem, cập nhật thông tin khách hàng
- Theo dõi công nợ từng khách hàng theo lịch sử từng lần thanh toán
- Hỗ trợ thanh toán nợ và đối chiếu dữ liệu

### Quản lý Nhà cung cấp
- Xem, thêm, sửa thông tin nhà cung cấp
- Tra cứu nhanh khi lập hóa đơn nhập

### Báo cáo & Thống kê
- Báo cáo sản phẩm bán chạy / bán chậm
- Báo cáo doanh thu theo tháng, quý, năm (dạng bảng và biểu đồ)

### Tài liệu dự án

| Tài liệu | Mô tả |
|---|---|
| `SRS.docx` | Software Requirement Specification — yêu cầu hệ thống, use case, business rules, wireframe |
| `SDD.docx` | Software Design Description — kiến trúc, sơ đồ lớp, thiết kế CSDL, screen flow |

---
### Ngoài phạm vi (Out of Scope)

- Quản lý nhân viên, chấm công, tính lương
- Tích hợp mã QR thanh toán
- Kết nối với hệ thống bên ngoài

---

### Thành viên nhóm

| Họ tên | Vai trò |
|---|---|
| Đinh Trương Đan Thuy | Trưởng nhóm |
| Hoàng Thị Kim Dung | Thành viên |
| **Lê Thị Nhung** | Thành viên |
| Đặng Như Trầm | Thành viên |
| Huỳnh Ngọc Thủy Tiên | Thành viên |

---

## Đóng góp cá nhân — Lê Thị Nhung

### Phân tích & Mô hình hóa
- Vẽ **Activity Diagram (AD)** mô tả luồng hoạt động của hệ thống
- Thiết kế **Use Case Diagram & Đặc tả Use Case:**
  - **UC_6 — Quản lý Khách hàng** (đầy đủ CRUD: Xem, Thêm, Sửa, Xóa)
  - **UC_5.3 — Đổi/Trả hàng**

### Viết tài liệu SRS
- **Mục 1 — Tổng quan (Overview):** Mục đích hệ thống (1.1 Purpose), bối cảnh vấn đề và định hướng giải pháp
- **Mục 4 — Non-functional Requirements:** Xác định các yêu cầu phi chức năng (hiệu năng, khả năng hỗ trợ, bảo mật,...)
- **Đặc tả màn hình** cho các chức năng được phân công

### Thiết kế Cơ sở dữ liệu (SDD)
- Vẽ **sơ đồ cơ sở dữ liệu**: Xây dựng sơ đồ thực thể mối quan hệ (ERD) cho hệ thống quản lý cửa hàng phụ tùng với cấu trúc 14 thực thể. 
- Thiết kế **vật lý cơ sở dữ liệu**: định nghĩa kiểu dữ liệu, ràng buộc, khóa chính/ngoại cho 14 bảng.

| Nhóm | Các bảng |
|---|---|
| Kho & Sản phẩm | `HangHoa`, `Gia` |
| Giao dịch Nhập | `HoaDonNhap`, `CT_HDN` |
| Giao dịch Bán | `HoaDonBan`, `CT_HDB`, `KhachHang` |
| Đối tác | `NhaCungCap` |
| Đổi trả | `PhieuDoiHang`, `CT_PhieuDoi` |
| Công nợ | `CongNo`, `CT_CongNo`, `CT_KhachTra` |
| Hệ thống | `TaiKhoan` |

### Thiết kế giao diện (Figma)
Thiết kế wireframe cho các màn hình:

| Nhóm chức năng | Màn hình |
|---|---|
| **Nhà cung cấp** | Xem danh sách · Xem chi tiết · Thêm · Sửa |
| **Khách hàng** | Xem danh sách · Xem chi tiết · Thêm · Sửa |
| **Hàng hóa** | Xem danh sách · Xem chi tiết · Thêm · Sửa |

---

### Thông tin đồ án

- **Môn học:** Phân Tích & Thiết Kế Hệ Thống Thông Tin  
- **Lớp:** 49K21.2 — Nhóm 49K212.08  
- **Trường:** Đại Học Kinh Tế — Đại Học Đà Nẵng  
- **Năm học:** 2025  
- **Địa điểm khảo sát:** Cửa hàng phụ tùng xe máy Tài, Thị trấn Di Lăng, Sơn Hà, Quảng Ngãi
