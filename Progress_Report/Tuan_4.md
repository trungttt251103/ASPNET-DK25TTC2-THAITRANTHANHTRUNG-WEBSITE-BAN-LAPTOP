# BÁO CÁO TIẾN ĐỘ ĐỒ ÁN - TUẦN 4

- **Thời gian thực hiện:** 13/07/2026 - 19/07/2026
- **Trọng tâm công việc:** Hiện thực hóa code chức năng quản trị (Phía Admin) và bổ sung tính năng cải tiến
- **Đề tài:** Xây dựng website bán laptop sử dụng ASP.NET MVC 5 và SQL Server

## 1. Nội dung công việc
- Tích hợp giao diện quản trị mẫu SB Admin 2 vào project phân hệ dành cho Admin.
- Thực hiện lập trình mã nguồn cho các bộ chức năng CRUD (Thêm, Đọc, Sửa, Xóa) quản lý các thực thể: Quản lý danh mục laptop, Quản lý thương hiệu/thể loại, Quản lý đơn hàng và Quản lý danh mục bài viết tin tức.
- Thiết lập giao diện trực quan phục vụ công tác Quản lý vai trò (Roles) và thiết lập cơ chế phân quyền truy cập.

## 2. Tài liệu liên quan
- Tài liệu tích hợp hệ thống bảo mật ASP.NET Identity API.
- Các tài liệu giải pháp phân quyền dựa trên vai trò (Role-based Authorization) để phân định biên giới chức năng giữa tài khoản Admin và tài khoản Khách hàng.

## 3. Khó khăn gặp phải
- Gặp trở ngại lớn khi nghiên cứu tích hợp các chức năng nâng cao theo đề xuất cải tiến: Thử nghiệm cơ chế thông báo nổi (Push Notification) thời gian thực khi có đơn hàng mới phát sinh gặp lỗi bất đồng bộ.
- Việc xây dựng logic gợi ý thông minh nhằm tự động đối soát, kiểm tra trùng khớp thông tin khách hàng cũ tại trang Admin để đưa ra đề xuất tạo mới profile hồ sơ tiêu tốn nhiều thời gian cấu hình nhưng hiệu quả chưa đạt tối ưu.

## 4. Kết quả đạt được
- Hoàn thiện toàn bộ hệ thống màn hình chức năng quản trị CRUD cốt lõi cho phân hệ Admin.
- Tích hợp thành công cơ chế phân quyền cơ bản giúp bảo vệ các router hệ thống khỏi các truy cập trái phép.
