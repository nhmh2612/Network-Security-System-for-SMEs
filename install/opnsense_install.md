# Hướng dẫn cài đặt & cấu hình OPNsense

## 1. Chuẩn bị
- Thiết bị firewall chuyên dụng hoặc máy ảo (Proxmox/VMware) hoặc là PC để tận hiến.
- Tối thiểu: 2 CPU, 2GB RAM, 20GB disk, 2 card mạng (WAN & LAN).

## 2. Cài đặt
1. Tải ISO: https://opnsense.org/download/
2. Boot từ ISO → chọn **Install OPNsense**.
3. Đặt mật khẩu `root` và cấu hình network ban đầu.
4. Reboot và truy cập web: `https://<IP-LAN>:443`

## 3. Cấu hình cơ bản
- Đặt IP cho WAN & LAN.
- Cho phép rule LAN → WAN.
- Chặn các port nguy hiểm (Telnet 23, SMB 445, …).

## 4. VPN
- Vào **VPN → OpenVPN**.
- Cấu hình Server Mode = Remote Access.
- Import CA và user certificate.
- Tải file cấu hình `.ovpn` cho client.

