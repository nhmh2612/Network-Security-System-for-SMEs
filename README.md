# Network-Security-System-for-SMEs
Dự án xây dựng hệ thống mạng bảo mật cho doanh nghiệp vừa và nhỏ (SMEs).

## 🚀 Tính năng chính
- Thiết kế mô hình mạng doanh nghiệp với **Cisco Packet Tracer**
- Firewall bảo mật với **OPNsense**
- Hệ thống giám sát & phát hiện xâm nhập với **Security Onion**
- Quản lý log và phân tích sự kiện bằng **Splunk**
- Quản lý Active Directory với **AD Manager Plus** và **AD Audit Plus**
- Quản lý hạ tầng mạng bằng **OpManager**
- Ảo hóa máy chủ với **Proxmox**

## 🛠️ Công nghệ sử dụng
- Cisco Packet Tracer
- OPNsense, Security Onion, Splunk
- ManageEngine AD Tools (Audit + Manager)
- Proxmox VE

## 📂 Cấu trúc repo
- `diagrams/` : Sơ đồ mạng & UML
- `configs/` : File cấu hình mẫu (firewall, VLAN)
- `configs/` : # File cấu hình, hướng dẫn
  
## Các thành phần chính trong hệ thống:
Router: Kết nối hệ thống nội bộ với mạng bên ngoài (External Network), là điểm đầu vào của dữ liệu từ bên ngoài.
Firewall: Bảo vệ hệ thống bằng cách lọc lưu lượng mạng đến và đi. Firewall sử dụng OPNsense, một nền tảng tường lửa nguồn mở.
Switch: Kết nối các phân đoạn mạng nội bộ, bao gồm:
  •	Tech: Khu vực kỹ thuật.
  •	Office: Văn phòng làm việc.
  •	WiFi: Hệ thống mạng không dây.
Monitor: Hệ thống giám sát hoạt động mạng sử dụng Security Onion (một nền tảng phát hiện và phân tích các mối đe dọa an ninh mạng).
Datacenter (Trung tâm dữ liệu): Lưu trữ Dữ liệu công ty (dữ liệu quan trọng phục vụ cho hoạt động doanh nghiệp).
Management Server (Máy chủ quản lý): Điều phối và quản lý hệ thống mạng:
  •	DNS Server: Quản lý tên miền nội bộ.
  •	AD Audit Plus: Giám sát và phân tích nhật ký Active Directory.
  •	OPManager: Quản lý hạ tầng mạng.
  •	Splunk: Phân tích dữ liệu và log.
  •	AD Manager: Quản lý tài khoản Active Directory.
Proxmox Virtual Environment: Cung cấp môi trường ảo hóa, với các tính năng như:
  • Quản lý tài nguyên hệ thống.
  • Remote làm việc từ xa (cho phép nhân viên làm việc từ xa an toàn).
