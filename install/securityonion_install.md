# Hướng dẫn cài đặt & cấu hình Security Onion

## 1. Chuẩn bị
- RAM: ≥ 8GB, CPU: 4 core, Disk: 200GB.
- NIC1: Management, NIC2: Monitoring.
- Tải ISO: https://securityonion.net

## 2. Cài đặt
1. Boot từ ISO → chọn **Install Security Onion**.
2. Đặt hostname, mật khẩu admin.
3. Chọn **Evaluation Mode** (test) hoặc **Production Mode** (thực tế).

## 3. Cấu hình sau cài đặt
```bash
sudo so-setup

- Chọn interface quản trị & giám sát.

- Bật Suricata, Zeek.

- Kích hoạt Kibana dashboard.

4. Truy cập

Web: https://<IP_Management>

Đăng nhập bằng admin đã tạo.