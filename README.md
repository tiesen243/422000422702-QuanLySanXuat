# Production Management System

Hệ thống web quản lý sản xuất bàn phím, hỗ trợ vận hành các nghiệp vụ từ đơn hàng, kế hoạch sản xuất, xưởng, kho, chất lượng, chấm công, lương đến hóa đơn.

## Tổng Quan

Ứng dụng được phát triển bằng PHP thuần theo kiến trúc MVC, hướng đến:

- Minh bạch hóa quy trình nghiệp vụ
- Hỗ trợ quản lý vận hành sản xuất
- Dễ dàng mở rộng và bảo trì

### Nghiệp Vụ Chính

- Tiếp nhận và quản lý đơn hàng
- Lập kế hoạch và điều phối sản xuất
- Quản lý xưởng sản xuất
- Quản lý kho nguyên vật liệu và thành phẩm
- Kiểm soát chất lượng
- Chấm công và tính lương nhân sự
- Xuất hóa đơn

## Công Nghệ Sử Dụng

| Thành phần | Công nghệ |
| ---------- | --------- |
| Front-end  | HTML, CSS, JavaScript |
| Back-end   | PHP (MVC) |
| Database   | MySQL |

## Cài Đặt

1. Sao chép `.env.example` thành `.env` và cập nhật thông tin kết nối.
2. Khởi tạo cơ sở dữ liệu từ `data/script.sql`.
3. Chạy ứng dụng bằng môi trường PHP/MySQL hoặc Docker Compose.

## Bản Quyền

Copyright (c) 2026. All rights reserved.
