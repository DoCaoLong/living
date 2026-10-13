# ÉLAN Living — Luxury Property Rental Demo (v1.1)

Demo website cho thuê căn hộ, nhà, villa với nền trắng ngà **#F3F4EE**.

## Chạy trên máy

Yêu cầu Node.js >=20.

```bash
npm install
npm run dev
```

Mở http://localhost:5173

## Các trang

- `/vi`, `/en`, `/ru`, `/ko`, `/zh`: 5 ngôn ngữ
- `/vi/properties`: danh sách, tìm kiếm, lọc giá, khu vực, loại hình, sắp xếp
- `/vi/properties/1`: chi tiết, ảnh và form thu lead
- `/vi/about`: giới thiệu, đội ngũ mẫu
- `/vi/contact`: thông tin công ty và form liên hệ
- `/admin`: quản trị demo (mật khẩu **demo123**)

## Admin demo

- Thêm/sửa/xóa bất động sản, chỉnh trạng thái (available/reserved/rented/hidden)
- Quản lý khách hàng từ biểu mẫu, cập nhật trạng thái lead, xuất CSV
- Dữ liệu lưu trong **localStorage của chính trình duyệt**; không đồng bộ giữa các máy.

## Cập nhật giao diện v1.1

- Hero mượt hơn: bỏ zoom lặp vô hạn, ưu tiên tải ảnh theo kích thước màn hình, hiệu ứng GSAP một lần trên desktop.
- Dropdown đổi ngôn ngữ thiết kế riêng cho 5 ngôn ngữ, chuyển tuyến trang tức thời không reload toàn bộ.
- GSAP: stagger các card BĐS, reveal nội dung khi cuộn, hiệu ứng ảnh editorial và thanh tiến độ cuộn trang.
- Tôn trọng `prefers-reduced-motion`, tinh chỉnh responsive trên mobile.
- Chi tiết xem `CHANGES.md`.

## Công nghệ

React 19, Vite 6, React Router 7, GSAP + ScrollTrigger, Lucide Icons, CSS thuần.

## Lưu ý trước khi triển khai production

Đây là **frontend demo**, không phải hệ thống production. Không có cơ sở dữ liệu, API, xác thực an toàn hay lưu lead trên server. Admin password `demo123` chỉ để demo và không bảo vệ dữ liệu thực. Cần tích hợp backend (Node.js + PostgreSQL/MongoDB), xác thực và phân quyền, upload ảnh, email notification, chống spam, kiểm tra dữ liệu và bảo vệ thông tin cá nhân. Nội dung BĐS chỉ có một phiên bản mô tả tiếng Anh; các chuỗi giao diện đã có 5 ngôn ngữ. Cần xây CMS hỗ trợ bản dịch cho title/description từng ngôn ngữ và SEO trước khi đi vào sử dụng. Ảnh đang lấy từ Unsplash và phụ thuộc internet, thay bằng ảnh đã được cấp quyền khi triển khai. Các liên hệ, tên nhân sự, testimonial hiện là placeholder cần thay bằng dữ liệu thực.

## Build

```bash
npm run build
npm run preview
```
