```markdown
# Hướng dẫn cài đặt & cấu hình Splunk

## 1. Chuẩn bị
- RAM: ≥ 8GB, CPU: 4 core, Disk: ≥ 100GB.
- OS: Ubuntu 20.04/22.04 hoặc Windows Server.

## 2. Cài đặt (Linux)
```bash
wget -O splunk-9.deb "https://download.splunk.com/products/splunk/releases/latest/linux/splunk.deb"
sudo dpkg -i splunk-9.deb
sudo /opt/splunk/bin/splunk enable boot-start
sudo /opt/splunk/bin/splunk start --accept-license

3. Cấu hình
Truy cập: http://<server>:8000

Tạo index: Settings → Indexes.

Thêm Data Input: syslog, firewall, AD log.

Tùy chỉnh dashboard (bar, pie, timechart).