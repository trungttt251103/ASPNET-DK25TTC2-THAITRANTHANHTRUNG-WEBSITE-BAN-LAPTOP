# BÁO CÁO TIẾN ĐỘ ĐỒ ÁN - TUẦN 3

- **Thời gian thực hiện:** 06/07/2026 - 12/07/2026
- **Trọng tâm công việc:** Hiện thực hóa code chức năng cốt lõi (Phía Khách hàng)
- **Đề tài:** Xây dựng website bán laptop sử dụng ASP.NET MVC 5 và SQL Server

## 1. Nội dung công việc
- Cấu hình chuỗi kết nối cơ sở dữ liệu (Connection String) trong file cấu hình hệ thống Web.config.
- Lập trình các bộ chức năng phía Khách hàng: Thiết kế phân hệ trang chủ, trang hiển thị danh sách sản phẩm, bộ lọc tìm kiếm sản phẩm thông minh theo Hãng sản xuất và Nhu cầu sử dụng.
- Xây dựng logic xử lý cho phân hệ Giỏ hàng (thêm laptop vào giỏ, điều chỉnh số lượng, xóa sản phẩm) và hoàn thiện luồng Quy trình đặt hàng trực tuyến cùng tính năng Xem lại lịch sử mua hàng.

## 2. Tài liệu liên quan
- Tài liệu kỹ thuật cấu hình định tuyến URL (ASP.NET Routing).
- Tài liệu hướng dẫn sử dụng ActionResults và cơ chế quản lý trạng thái Session trong ASP.NET để lưu trữ thông tin giỏ hàng tạm thời.

## 3. Khó khăn gặp phải
- Việc đồng bộ hóa dữ liệu giỏ hàng khi người dùng thay đổi số lượng trực tiếp trên giao diện front-end mà không làm tải lại toàn bộ trang (Page reload) gặp nhiều lỗi logic. Giải pháp khắc phục là nghiên cứu và áp dụng kỹ thuật gọi AJAX kết hợp xử lý qua jQuery.

## 4. Kết quả đạt được
- Vận hành ổn định luồng xử lý mua hàng cốt lõi từ bước tiếp cận sản phẩm, đưa vào giỏ hàng cho đến bước xác nhận đơn hàng và lưu dữ liệu thành công xuống cơ sở dữ liệu.
