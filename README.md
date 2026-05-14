# cook-pad
# ĐỒ ÁN MÔN HỌC: CHUYÊN ĐỀ ASP.NET
## Đề tài: Hệ thống chia sẻ công thức nấu ăn trực tuyến (Cookpad Clone)

---

### 1. THÔNG TIN SINH VIÊN
* **Họ và tên:** [Họ và tên của bạn]
* **Mã lớp:** [Mã lớp của bạn]
* [cite_start]**Tên Repository:** ASPNET-[malop]-[hotenkhongdau]-COOKPAD [cite: 65]
* [cite_start]**Email liên lạc:** [Địa chỉ email của bạn] [cite: 95]
* [cite_start]**Số điện thoại:** [Số điện thoại của bạn] [cite: 95]

---

### 2. GIỚI THIỆU ĐỒ ÁN
* [cite_start]**Mục tiêu:** Xây dựng ứng dụng web cho phép người dùng đăng tải, tìm kiếm và quản lý công thức nấu ăn[cite: 19].
* **Công nghệ sử dụng:**
    * [cite_start]**Backend:** ASP.NET Core Web API[cite: 21].
    * [cite_start]**Frontend:** React.js[cite: 21].
    * [cite_start]**Cơ sở dữ liệu:** SQL Server[cite: 21].
* **Trạng thái:** Đang thực hiện.

---

### [cite_start]3. CẤU TRÚC THƯ MỤC REPOSITORY [cite: 78]
Dự án được tổ chức theo quy định bắt buộc của tài liệu hướng dẫn:

* [cite_start]**`/setup`**: Chứa tập tin cài đặt chương trình, SQL script khởi tạo dữ liệu[cite: 80].
* [cite_start]**`/scr`**: Chứa toàn bộ mã nguồn chương trình (Backend API & Frontend React)[cite: 82].
* [cite_start]**`/progress-report`**: [Bắt buộc] Chứa các file báo cáo tiến độ hàng tuần (.pdf/.docx)[cite: 83].
* [cite_start]**`/thesis`**: [Bắt buộc] Tài liệu văn bản của đồ án[cite: 84]:
    * [cite_start]`/doc`: Chứa tài liệu định dạng .DOC[cite: 87].
    * [cite_start]`/pdf`: Chứa tài liệu định dạng .PDF[cite: 88].
    * [cite_start]`/refs`: Chứa các tài liệu tham khảo khi thực hiện đồ án[cite: 91].
    * [cite_start]`/abs`: Chứa slide báo cáo (.PPT), video demo (.AVI)[cite: 90].
* [cite_start]**`/docker`**: Chứa các file cấu hình triển khai ứng dụng trên Docker (nếu có)[cite: 94].

---

### [cite_start]4. QUY ĐỊNH VỀ TIẾN ĐỘ [cite: 63]
* [cite_start]**Quản lý:** Đồ án được quản lý hoàn toàn qua GitHub[cite: 62].
* [cite_start]**Giảng viên hướng dẫn:** Đã mời `antonio86doan@gmail.com` làm Collaborator[cite: 66, 67].
* [cite_start]**Commit:** Cam kết commit code thường xuyên (ít nhất 1 lần/tuần) theo nội dung thực hiện thực tế[cite: 70].
* [cite_start]**Báo cáo:** Cập nhật file báo cáo tuần vào thư mục `progress-report` đúng hạn[cite: 73].

---

### 5. HƯỚNG DẪN CÀI ĐẶT (DỰ KIẾN)
[cite_start]*(Phần này sẽ cập nhật chi tiết khi hoàn thiện mã nguồn tại `/scr`) [cite: 69]*

1. Clone repository về máy.
2. Chạy script SQL trong `/setup` để tạo database.
3. Cấu hình chuỗi kết nối trong `appsettings.json` của Backend.
4. Chạy Backend bằng lệnh `dotnet run`.
5. Cài đặt thư viện Frontend bằng `npm install` và chạy bằng `npm start`.

---
[cite_start]*File README.md này sẽ được cập nhật liên tục trong suốt quá trình nghiên cứu và thực hiện đồ án[cite: 69].*