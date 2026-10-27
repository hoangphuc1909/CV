# Portfolio CV cá nhân

> Trang portfolio giới thiệu cá nhân, kỹ năng, dự án và thông tin liên hệ. Giao diện được xây dựng theo hướng responsive, ưu tiên thiết bị di động và sử dụng HTML/CSS thuần.

## Tên dự án

**Portfolio CV cá nhân** (bài tập A2.1).

## Mô tả

Đây là website tĩnh một trang dành cho Frontend Developer. Người xem có thể tìm hiểu phần giới thiệu, kỹ năng, các dự án tiêu biểu và cách liên hệ. Trang sử dụng các liên kết neo để điều hướng giữa các mục và bố cục tự điều chỉnh theo kích thước màn hình.

## Chức năng

- Hiển thị phần giới thiệu và vai trò nghề nghiệp.
- Trình bày danh sách kỹ năng và các dự án mẫu.
- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp liên kết email, GitHub và LinkedIn.
- Hỗ trợ bố cục trên điện thoại, máy tính bảng và máy tính để bàn.

## Công nghệ

- HTML5: cấu trúc ngữ nghĩa và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid và responsive design.
- Nginx (tùy chọn): phục vụ website trong Docker.

Trang không cần Node.js, trình quản lý gói hay bước biên dịch.

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm phần mềm.
- Để chạy máy chủ cục bộ: Python 3 (tùy chọn).
- Để chạy bằng container: Docker Engine hoặc Docker Desktop đang hoạt động.
- Kết nối Internet chỉ cần thiết nếu bạn bổ sung tài nguyên bên ngoài; các tài nguyên hiện có của trang nằm trong dự án hoặc được nhúng trực tiếp.

## Cấu trúc dự án

```text
.
├── index.html
├── README.md
└── assets/
	├── css/
	│   └── styles.css
	└── img/
```

## Cài đặt

Không cần cài đặt thư viện. Tải hoặc sao chép toàn bộ dự án về máy, sau đó mở thư mục dự án trong terminal hoặc trình quản lý tệp.

## Cấu hình

Website không sử dụng tệp cấu hình môi trường hay khóa API. Để cá nhân hóa nội dung, chỉnh sửa `index.html`:

- Cập nhật tên, phần giới thiệu và chức danh trong phần đầu trang.
- Thay ảnh `assets/img/avatar.jpg` bằng ảnh đại diện của bạn (hoặc cập nhật đường dẫn ảnh).
- Cập nhật mô tả, liên kết và công nghệ của từng dự án.
- Thay email, GitHub và LinkedIn mẫu bằng thông tin liên hệ thật.
- Kiểm tra và thống nhất tên tác giả trong tiêu đề, metadata, nội dung, văn bản thay thế ảnh và chân trang trước khi công khai. Bản hiện tại còn một số nội dung mẫu chưa đồng nhất.

Để thay đổi giao diện, chỉnh sửa `assets/css/styles.css`.

## Chạy thử

### Windows

**Mở trực tiếp:** mở `index.html` bằng trình duyệt.

**Chạy máy chủ cục bộ bằng Python 3 (PowerShell):**

```powershell
cd "duong-dan\toi\du-an"
py -m http.server 8000
```

Nếu lệnh `py` không có, thử `python -m http.server 8000`. Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### macOS

**Mở trực tiếp:** mở `index.html` bằng Safari hoặc trình duyệt khác.

**Chạy máy chủ cục bộ bằng Python 3:**

```bash
cd "/duong-dan/toi/du-an"
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Linux

**Mở trực tiếp:** mở `index.html` bằng trình duyệt.

**Chạy máy chủ cục bộ bằng Python 3:**

```bash
cd "/duong-dan/toi/du-an"
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Nếu chưa có Python 3, cài đặt bằng trình quản lý gói của bản phân phối Linux. Dừng máy chủ bằng `Ctrl+C`.

### Docker

Cần cài và khởi động Docker trước. Chạy lệnh từ thư mục gốc của dự án; container Nginx sẽ phục vụ các tệp hiện tại ở cổng `8080` mà không cần tạo Dockerfile:

**macOS/Linux:**

```bash
docker run --rm --name portfolio -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

**Windows PowerShell:**

```powershell
docker run --rm --name portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080>. Dừng container bằng `Ctrl+C`. Nếu cổng `8080` đang được sử dụng, thay phần `8080:80` bằng một cổng trống, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

Thông tin đang được khai báo trong mục **Liên hệ** của `index.html`:

- Email: `an.nguyen@example.com` (địa chỉ mẫu).
- GitHub: `github.com/nguyenvanan` (liên kết mẫu).
- LinkedIn: `linkedin.com/in/nguyenvanan` (liên kết mẫu).

Đây là dữ liệu mẫu, không xác nhận thông tin liên hệ thật của tác giả. Hãy thay bằng thông tin chính xác trước khi chia sẻ website; đồng thời thống nhất tên tác giả trong nội dung trang.

