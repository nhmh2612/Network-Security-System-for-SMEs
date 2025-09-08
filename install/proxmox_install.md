# Hướng dẫn cài đặt & cấu hình Proxmox VE

## 1. Chuẩn bị
- Máy chủ vật lý.
- RAM: ≥ 16GB, CPU hỗ trợ ảo hóa.
- Disk: ≥ 500GB.

## 2. Cài đặt
1. Tải ISO: https://www.proxmox.com/en/downloads
2. Boot từ ISO → chọn **Install Proxmox VE**.
3. Đặt root password, email.
4. Cấu hình network (IP tĩnh).

## 3. Quản lý
- Truy cập web: `https://<IP>:8006`.
- Tạo VM (KVM) hoặc container (LXC).
- Quản lý storage, backup, replication.
