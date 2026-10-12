# SS10 - Bài 2: Single-stage Dockerfile

Ứng dụng REST API đơn giản bằng Node.js/Express được đóng gói với Dockerfile Single-stage.

## Build image

```bash
docker build -t hw-backend:v1 .
```

## Chạy container

```bash
docker run -d --name app-single-stage -p 8080:3000 hw-backend:v1
```

## Kiểm tra

```bash
docker ps
docker logs app-single-stage
curl -i http://localhost:8080/
```

Kết quả dự kiến: HTTP 200 và JSON `{"status":"success","message":"Hello from Docker Single-stage!"}`.

## Minh chứng

Chèn ảnh chụp kết quả build image, `docker ps`, `docker logs` và `curl` trước khi nộp.
