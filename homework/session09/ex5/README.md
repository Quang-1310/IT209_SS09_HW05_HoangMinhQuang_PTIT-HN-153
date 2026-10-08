## Mục tiêu

Khởi chạy một dịch vụ web Nginx bằng Docker Compose CLI v2 và ánh xạ cổng `8082` của máy host tới cổng `80` của container.

## Yêu cầu

- Docker và Docker Compose CLI v2 đã được cài đặt.
- Docker Engine đang chạy.

## Cách chạy

Tại thư mục chứa tệp `docker-compose.yml`, khởi chạy dịch vụ ở chế độ nền:

```bash
docker compose up -d
```

Kiểm tra trạng thái dịch vụ:

```bash
docker compose ps
```

Kiểm tra trang web Nginx:

```bash
curl http://localhost:8082
```

Kết quả mong đợi là service `web` đang chạy trên cổng `8082` và lệnh `curl` trả về trang chào mừng của Nginx.

## Dừng và xóa dịch vụ

```bash
docker compose down
```