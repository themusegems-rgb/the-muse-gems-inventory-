# The Muse Gems – Hệ thống quản lý kho hàng

## 1. Tổng quan dự án (Project Overview)

**The Muse Gems Inventory Management System** là hệ thống quản lý kho được xây dựng nhằm hỗ trợ The Muse Gems quản lý, theo dõi và kiểm soát số lượng hàng hóa trong kho.

Hệ thống được phát triển bằng **Google AppSheet** làm nền tảng ứng dụng và **Google Sheets** làm cơ sở dữ liệu.

## 2. Mục tiêu dự án (Project Objectives)

- Quản lý danh mục sản phẩm, sản phẩm và các biến thể sản phẩm.
- Theo dõi số lượng tồn kho thực tế, số lượng hàng đang được giữ và số lượng hàng khả dụng.
- Ghi nhận các giao dịch nhập kho và xuất kho.
- Quản lý hàng hoàn và các sản phẩm bị lỗi.
- Hỗ trợ kiểm kê và điều chỉnh tồn kho.
- Quản lý hoạt động tạm giữ hàng.
- Hỗ trợ lập báo cáo tình hình tồn kho.

## 3. Công nghệ sử dụng (Technology Stack)

| Thành phần | Công nghệ |
|---|---|
| Nền tảng ứng dụng | Google AppSheet |
| Cơ sở dữ liệu | Google Sheets |
| Xác thực người dùng | AppSheet Authentication / Tài khoản Google |
| Quản lý dữ liệu | AppSheet Data Operations |
| Tự động hóa | AppSheet Automation |
| Lưu trữ tài liệu và quản lý phiên bản | GitHub |

## 4. Các chức năng chính (Main System Features)

- Quản lý danh mục sản phẩm.
- Quản lý sản phẩm và biến thể sản phẩm.
- Quản lý tồn kho.
- Quản lý giao dịch nhập kho và xuất kho.
- Quản lý hàng tạm giữ.
- Quản lý hàng hoàn bị lỗi.
- Kiểm kê và điều chỉnh tồn kho.
- Thống kê và báo cáo tồn kho.
- Phân quyền truy cập theo vai trò người dùng.

## 5. Cấu trúc cơ sở dữ liệu (Database Structure)

Hệ thống sử dụng 8 bảng dữ liệu chính:

1. Category – Danh mục sản phẩm.
2. Product – Sản phẩm.
3. Product_Variant – Biến thể sản phẩm.
4. Inventory_Stock – Tồn kho.
5. Stock_Reservation – Thông tin giữ hàng.
6. User – Người dùng.
7. Inventory_Transaction – Phiếu giao dịch kho.
8. Transaction_Item – Chi tiết giao dịch kho.

Tham khảo thư mục `database/` để xem sơ đồ ERD, cấu trúc cơ sở dữ liệu và từ điển dữ liệu.

## 6. Kiến trúc hệ thống (System Architecture)

Hệ thống được tổ chức theo mô hình kiến trúc ba tầng đơn giản:

- **Client/UI:** Giao diện Google AppSheet được truy cập thông qua trình duyệt web và thiết bị di động.
- **Application/Backend:** Google AppSheet xử lý logic nghiệp vụ, xác thực người dùng, thao tác dữ liệu và tự động hóa.
- **Database:** Google Sheets được sử dụng để lưu trữ dữ liệu của hệ thống.

Hệ thống sử dụng cơ chế xác thực tài khoản Google thông qua AppSheet.

Tham khảo file `docs/03_system_architecture.md` để biết thêm chi tiết về kiến trúc hệ thống.

## 7. Cấu trúc Repository (Repository Structure)

- `docs/`: Lưu trữ tài liệu dự án, yêu cầu hệ thống, kiến trúc và quy trình nghiệp vụ.
- `database/`: Lưu trữ sơ đồ ERD, cấu trúc cơ sở dữ liệu, từ điển dữ liệu và dữ liệu mẫu.
- `app_design/`: Lưu trữ bản thiết kế giao diện, wireframe và báo cáo.
- `app_config/`: Lưu trữ công thức AppSheet, cấu hình tự động hóa và phân quyền.
- `source/`: Lưu trữ mã nguồn nếu có hoặc tài liệu kỹ thuật về quá trình triển khai ứng dụng.
- `demo/`: Lưu trữ hình ảnh, video minh họa và bản prototype của hệ thống.
- `project_management/`: Lưu trữ thông tin thành viên, phân công công việc và biên bản họp nhóm.

## 8. Hướng dẫn truy cập hệ thống (Getting Started)

Ứng dụng được xây dựng và triển khai trên nền tảng Google AppSheet.

Các bước truy cập hệ thống:

1. Được chủ sở hữu ứng dụng cấp quyền truy cập.
2. Đăng nhập bằng tài khoản Google đã được cấp quyền.
3. Truy cập ứng dụng thông qua đường dẫn AppSheet được cung cấp.
4. Sử dụng các chức năng tương ứng với vai trò người dùng được phân quyền.

**Lưu ý:** Repository này chứa tài liệu và các sản phẩm bàn giao của dự án. Ứng dụng AppSheet và cơ sở dữ liệu Google Sheets thực tế được quản lý trên các nền tảng tương ứng.

## 9. Thành viên nhóm (Team Members)

| STT | Họ và tên | Vai trò |
|---|---|---|
| 1 | Trương Thị Thảo Vân | [Vai trò] |
| 2 | Nguyễn Trần Lê Vy | [Vai trò] |
| 3 | Lê Hoàng Trang | [Vai trò] |

## 10. Sản phẩm bàn giao (Project Deliverables)

- Tài liệu mô tả yêu cầu dự án.
- Tài liệu Use Case và quy trình nghiệp vụ.
- Sơ đồ kiến trúc hệ thống.
- Sơ đồ quan hệ thực thể (ERD).
- Cấu trúc cơ sở dữ liệu và từ điển dữ liệu.
- Thiết kế giao diện ứng dụng AppSheet.
- Bản demo hệ thống.
- Báo cáo tổng kết dự án.

## 11. Trạng thái dự án (Project Status)

**Trạng thái:** Đang phát triển (In Development).

---

*The Muse Gems – Hệ thống quản lý kho hàng*
