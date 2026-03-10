# Network-Security-System-for-SMEs
Dự án xây dựng hệ thống mạng bảo mật cho doanh nghiệp vừa và nhỏ (SMEs).

## Tính năng chính
- Thiết kế mô hình mạng doanh nghiệp với **Cisco Packet Tracer**
- Firewall bảo mật với **OPNsense**
- Hệ thống giám sát & phát hiện xâm nhập với **Security Onion**
- Quản lý log và phân tích sự kiện bằng **Splunk**
- Quản lý Active Directory với **AD Manager Plus** và **AD Audit Plus**
- Quản lý hạ tầng mạng bằng **OpManager**
- Ảo hóa máy chủ với **Proxmox**

## Công nghệ sử dụng
- Cisco Packet Tracer
- OPNsense, Security Onion, Splunk
- ManageEngine AD Tools (Audit + Manager)
- Proxmox VE

## Cấu trúc repo
- `diagrams/` : Sơ đồ mạng & UML
- `configs/` : File cấu hình mẫu (firewall, VLAN)
- `docs/` : Tài liệu tổng quan
- `install/` : Hướng dẫn cài đặt & cấu hình chi tiết

## Các thành phần chính trong hệ thống
- **Router**: Kết nối hệ thống nội bộ với mạng bên ngoài (External Network), là điểm đầu vào của dữ liệu từ bên ngoài.  
- **Firewall (OPNsense)**: Bảo vệ hệ thống bằng cách lọc lưu lượng mạng đến và đi.  
- **Switch**: Kết nối các phân đoạn mạng nội bộ, bao gồm:  
  - Tech: Khu vực kỹ thuật  
  - Office: Văn phòng làm việc  
  - WiFi: Hệ thống mạng không dây  
- **Monitor (Security Onion)**: Hệ thống giám sát hoạt động mạng, phát hiện và phân tích các mối đe dọa an ninh.  
- **Datacenter (Trung tâm dữ liệu)**: Lưu trữ dữ liệu quan trọng phục vụ cho hoạt động doanh nghiệp.  
- **Management Server (Máy chủ quản lý)**: Điều phối và quản lý hệ thống mạng, bao gồm:  
  - DNS Server: Quản lý tên miền nội bộ  
  - AD Audit Plus: Giám sát và phân tích nhật ký Active Directory  
  - OpManager: Quản lý hạ tầng mạng  
  - Splunk: Phân tích dữ liệu và log  
  - AD Manager: Quản lý tài khoản Active Directory  
- **Proxmox Virtual Environment**: Cung cấp môi trường ảo hóa, với các tính năng:  
  - Quản lý tài nguyên hệ thống  
  - Remote làm việc từ xa (cho phép nhân viên làm việc từ xa an toàn)

## Tài liệu tổng quan (`docs/`)
- [1. Thiết kế mạng](docs/1_network_design.md)  
- [2. Firewall OPNsense](docs/2_firewall_opnsense.md)  
- [3. IDS Security Onion](docs/3_ids_securityonion.md)  
- [4. Splunk](docs/4_splunk.md)  
- [5. Active Directory](docs/5_ad_management.md)  
- [6. OpManager](docs/6_opmanager.md)  
- [7. Proxmox](docs/7_proxmox.md)  
- [8. Tổng kết](docs/8_summary.md)  

---

## Hướng dẫn cài đặt chi tiết (`install/`)
- [Cài đặt OPNsense](install/opnsense_install.md)  
- [Cài đặt Security Onion](install/securityonion_install.md)  
- [Cài đặt Splunk](install/splunk_install.md)  
- [Cài đặt AD Manager & AD Audit Plus](install/ad_management_install.md)  
- [Cài đặt OpManager](install/opmanager_install.md)  
- [Cài đặt Proxmox VE](install/proxmox_install.md)  

---

## Các thành phần chính trong hệ thống
- **Router**: Kết nối hệ thống nội bộ với Internet.  
- **Firewall (OPNsense)**: Lọc lưu lượng, bảo mật mạng.  
- **Switch**: Chia VLAN (Tech, Office, WiFi).  
- **Security Onion**: Giám sát & phát hiện xâm nhập.  
- **Datacenter**: Lưu trữ dữ liệu quan trọng.  
- **Management Server**:  
  - DNS Server  
  - AD Audit Plus  
  - OpManager  
  - Splunk  
  - AD Manager  
- **Proxmox VE**: Ảo hóa máy chủ, hỗ trợ remote work an toàn.  
---
Yêu cầu phần cứng (Hardware Requirements)

Để triển khai hệ thống trong môi trường lab hoặc demo, cần chuẩn bị máy chủ ảo hóa (Proxmox) với tài nguyên tối thiểu khoảng:

Khuyến nghị tổng tài nguyên:

CPU: 8 vCPU trở lên

RAM: 24–32 GB

Storage: 300–500 GB SSD

Phân bổ tài nguyên cho từng dịch vụ
Service	CPU	RAM	Storage	Ghi chú
OPNsense Firewall	2 vCPU	2 GB	20 GB	Firewall & NAT
Security Onion (IDS/SIEM)	4 vCPU	8 GB	100 GB	Phân tích log & IDS
Splunk Server	2–4 vCPU	8 GB	100 GB	Thu thập & phân tích log
Active Directory (Windows Server)	2 vCPU	4 GB	40 GB	Domain Controller
AD Manager + AD Audit Plus	2 vCPU	4 GB	40 GB	Quản lý AD
OpManager	2 vCPU	4 GB	40 GB	Monitoring hệ thống
DNS Server	1 vCPU	1 GB	10 GB	DNS nội bộ
Client Simulator	1 vCPU	2 GB	20 GB	Máy client mô phỏng
Proxmox Host	—	—	—	Máy chủ ảo hóa
Lưu ý

Security Onion và Splunk tiêu thụ nhiều tài nguyên nhất do xử lý log và traffic.

Nếu chạy trên máy cá nhân, có thể giảm tài nguyên để tiết kiệm RAM:

Splunk: 4GB RAM

Security Onion: 6GB RAM

Nên sử dụng SSD để tăng hiệu suất xử lý log và truy vấn dữ liệu.

Nếu triển khai trong môi trường doanh nghiệp thực tế, nên tách SIEM (Splunk) và IDS (Security Onion) sang các máy chủ riêng để đảm bảo hiệu năng. 
---
