# BÁO CÁO TIẾN ĐỘ ĐỒ ÁN - TUẦN 2

- **Thời gian thực hiện:** 29/06/2026 - 05/07/2026
- **Trọng tâm công việc:** Phân tích thiết kế hệ thống và Cơ sở dữ liệu
- **Đề tài:** Xây dựng website bán laptop sử dụng ASP.NET MVC 5 và SQL Server

## 1. Nội dung công việc
- Khảo sát thực tế nhu cầu, quy trình vận hành và quản lý tại cửa hàng kinh doanh máy tính để định hình nghiệp vụ.
- Xác định và đặc tả chi tiết yêu cầu chức năng (gồm 14 chức năng chính phân chia cho phân hệ Khách hàng và Admin) cùng các yêu cầu phi chức năng (bảo mật dữ liệu, hiệu năng, độ tương thích giao diện).
- Xây dựng sơ đồ Use-case tổng quát mức 0 để mô tả luồng tương tác của các tác nhân.
- Thiết kế mô hình quan hệ dữ liệu (ERD) trực tiếp trên hệ quản trị cơ sở dữ liệu SQL Server.

## 2. Tài liệu liên quan
- Tài liệu chuyên ngành phân tích thiết kế hệ thống thông tin.
- Cẩm nang hướng dẫn quản trị và tối ưu cơ sở dữ liệu SQL Server.
- Tài liệu đặc tả cấu trúc các bảng phân quyền mặc định của thư viện Identity (AspNetUsers, AspNetRoles,...) và các bảng nghiệp vụ bán hàng tự thiết kế (Laptop, Hang, TinTuc, ChuDe, BinhLuan).

## 3. Khó khăn gặp phải
- Thiết kế mối quan hệ ràng buộc khóa chính/khóa ngoại lồng ghép giữa các thực thể cốt lõi là Laptop, MetaLaptop và Hang tương đối phức tạp.
- Khó khăn trong việc tìm giải pháp kết nối đồng bộ hệ thống phân quyền có sẵn của ASP.NET Identity với cấu trúc dữ liệu nghiệp vụ riêng của website bán laptop.

## 4. Kết quả đạt được
- Hoàn thiện Từ điển dữ liệu chi tiết cho toàn bộ hệ thống bao gồm 14 bảng dữ liệu cụ thể.
- Xây dựng thành công sơ đồ cơ sở dữ liệu (Database Schema) hoàn chỉnh, sẵn sàng cho việc kết nối và lập trình mã nguồn ở tuần kế tiếp.
