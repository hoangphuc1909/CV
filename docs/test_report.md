# Báo cáo kiểm thử

## Thông tin kiểm thử

- Ngày kiểm thử: 27/10/2026.
- Nền tảng: Windows, Google Chrome.
- Cách chạy: mở trực tiếp `index.html` bằng trình duyệt (`file://`).
- Kích thước chụp: desktop 1440 × 1000 px; mobile 390 × 844 px.
- Phương pháp: kiểm tra trực quan trên trình duyệt, kiểm tra DOM/liên kết/ảnh bằng trình duyệt và rà soát mã nguồn. Đây không phải kiểm thử bảo mật chuyên sâu.

## Kết quả theo tiêu chí

### 1. Tính đúng đắn — Đạt một phần

- Trang tải được; các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ hiển thị.
- Các liên kết điều hướng đến `#about`, `#skills`, `#projects`, `#contact` và `#top` đều có phần tử đích tương ứng.
- Cả 5 ảnh trên trang đều tải thành công trong lần kiểm tra.
- Các nút “Xem chi tiết” và liên kết GitHub/LinkedIn đang dùng `href="#"`, chưa dẫn tới trang đích thực tế.

### 2. UI/UX — Đạt một phần

- Ở desktop, bố cục giới thiệu, thanh điều hướng và danh sách kỹ năng hiển thị rõ ràng.
- Ở mobile, ảnh chụp cho thấy nội dung phần giới thiệu và ảnh đại diện có dấu hiệu bị cắt ở mép phải. CSS đang đặt `overflow-x: hidden`, có thể che phần tràn thay vì giải quyết nguyên nhân. Cần chỉnh và chụp kiểm thử lại trước khi kết luận responsive đạt.
- Ảnh desktop chỉ ghi lại phần đầu trang, không bao gồm toàn bộ trang trong cùng một khung hình.

### 3. Khả năng vận hành - xử lý lỗi — Đạt một phần

- Website tĩnh mở được trực tiếp từ tệp HTML và các ảnh hiện có tải thành công.
- Trang không có JavaScript, biểu mẫu, API hay thao tác ghi dữ liệu nên không phát sinh luồng xử lý lỗi ứng dụng để kiểm thử. Chưa kiểm thử lỗi máy chủ hoặc lỗi mạng khi triển khai.

### 4. Bảo mật — Đạt trong phạm vi rà soát tĩnh

- Mã nguồn hiện không có JavaScript, biểu mẫu nhập liệu, khóa API hay thông tin bí mật được nhúng.
- Trang không gọi thư viện hoặc script bên thứ ba trong mã HTML đã kiểm tra.
- Đánh giá này chỉ áp dụng cho website tĩnh hiện tại; chưa thực hiện kiểm thử xâm nhập, cấu hình máy chủ hoặc kiểm tra bảo mật khi triển khai.

### 5. Chất lượng mã nguồn — Đạt một phần

- HTML dùng các phần tử ngữ nghĩa như `header`, `nav`, `main`, `section`, `article` và `footer`; CSS được tách riêng.
- CSS có biến dùng chung, bố cục Flexbox/Grid, breakpoint responsive, trạng thái `focus-visible` và hỗ trợ `prefers-reduced-motion`.
- Tên tác giả chưa đồng nhất giữa metadata, tiêu đề, nội dung, alt ảnh và chân trang; một số liên kết còn là giá trị mẫu.

### 6. Khả năng triển khai — Đạt một phần

- Có thể triển khai như website tĩnh vì dự án không cần bước build hay cài thư viện.
- Đã kiểm tra mở trang từ tệp cục bộ; chưa triển khai lên hosting/web server và chưa chạy thử bằng Docker.
- Dự án hiện không có Dockerfile hoặc cấu hình triển khai tự động. Nếu triển khai thực tế, cần kiểm tra đường dẫn tài nguyên và thay các dữ liệu liên hệ/liên kết mẫu.

## Minh chứng

Ảnh được chụp từ trang đang chạy trong Chrome và lưu trong `docs/screenshots/`:

- Desktop: [screenshots/desktop.png](screenshots/desktop.png)
- Mobile: [screenshots/mobile.png](screenshots/mobile.png)
