# Dịch vụ Gateway

Thư mục này chứa cấu hình cho Kong Gateway được sử dụng trong nền tảng HRM-MS.

## Cấu trúc

- `docker-compose.yml`: Tệp Docker Compose để thiết lập gateway.
- `kong/kong.yml`: Tệp cấu hình cho Kong Gateway.

## Cấu hình Kong

Tệp `kong/kong.yml` định nghĩa các dịch vụ và tuyến đường cho gateway. Ví dụ:

- **Dịch vụ**: `example_service`
  - Host: `httpbin.konghq.com`
  - Port: `80`
  - Giao thức: `http`
- **Tuyến đường**: `example_route`
  - Đường dẫn: `/mock`
  - Loại bỏ đường dẫn: `true`

## Sử dụng

1. Đảm bảo Docker đã được cài đặt và đang chạy.
2. Sử dụng `docker-compose` để khởi động gateway:

   ```bash
   docker-compose up -d
   ```

3. Truy cập các tuyến đường được cấu hình thông qua gateway.
