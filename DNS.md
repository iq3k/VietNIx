**1. DNS Là Gì?**
DNS (Domain Name System) là hệ thống phân giải tên miền – chuyển đổi tên miền (ví dụ: www.google.com) thành địa chỉ IP (ví dụ: 142.250.190.4) để máy tính có thể giao tiếp với nhau.

**2. Cách DNS Hoạt Động Cơ Bản**
Khi truy cập vào một website:
- Trình duyệt gửi yêu cầu đến DNS Resolver (thường do ISP cung cấp).
- Resolver truy vấn lên DNS Root Server, Top-Level Domain (TLD), rồi đến Authoritative DNS Server.
- Authoritative server trả về địa chỉ IP của tên miền đó.
- Trình duyệt dùng địa chỉ IP để kết nối tới server web.
![image](https://hackmd.io/_uploads/HkFFlJ6pkx.png)
![image](https://hackmd.io/_uploads/ByHn-k6Tyl.png)


**3. Các Thành Phần Của DNS**

- DNS Resolver: Máy chủ đầu tiên xử lý truy vấn DNS
- Root Server: Máy chủ gốc phân phối truy vấn tới các TLD
- TLD Server: Máy chủ tên miền cấp cao nhất (.com, .net, .vn…)
- Authoritative Server: Máy chủ có thông tin chính xác cuối cùng cho tên miền

**4. Các Bản Ghi DNS Phổ Biến (DNS Records)**
- A record:	Trỏ tên miền tới địa chỉ IPv4
- AAAA record: Trỏ tên miền tới địa chỉ IPv6
- CNAME: Bí danh, trỏ tên miền này sang tên miền khác
- MX: Chỉ định máy chủ email (Mail Exchange)
- NS: Máy chủ tên (Name Server) của tên miền
TXT	Lưu thông tin dạng văn bản (dùng cho SPF, DKIM, xác minh Google, v.v.)
- PTR: Phân giải ngược từ IP → domain (dùng trong Reverse DNS)
- SRV: Dùng để xác định dịch vụ (ít phổ biến hơn)

**5. TTL (Time to Live) Là Gì?**
TTL là thời gian trình duyệt hoặc DNS Resolver lưu cache bản ghi DNS. Giá trị nhỏ → cập nhật nhanh hơn, nhưng tăng tải hệ thống.

**6. Forward DNS vs Reverse DNS**
Forward DNS: Domain → IP (phổ biến)

Reverse DNS (rDNS): IP → Domain (dùng trong email, bảo mật)

**7. DNS Caching**
DNS Resolver thường lưu lại bản ghi DNS một thời gian (theo TTL) để tăng tốc độ truy cập và giảm tải hệ thống.

**8.Command**
- nslookup [tham số] vietnix.vn: truy vấn DNS cơ bản của vietnix.vn; tham số: -type=NS, A, MX,... để kiểm tra bản ghi.
- dig [tham số] vietnix.vn: truy vấn DNS nâng cao của vietnix.vn; tham số: A, NS, MX, ANY,... để xem chi tiết bản ghi.
- cat /etc/resolv.conf: xem DNS server đang dùng.
- systemctl restart systemd-resolved: Xóa cache DNS (Ubuntu)