# Sản phẩm của VietNix
## Hosting
- Domain hay tên miền là địa chỉ trang web hoạt động trên Internet. Nói cách khác domain là mặt mạ cho địa chỉ ip của máy chủ trang web thay vì phải gõ các số phức tạp để truy cập vào ip của máy chủ thì ta thể dễ dàng truy cập bằng domain.
- Cấu trúc của domain: protocol, sub domain, second level doamin (sld), top level domain (tld), page path.
- Tổ chức quản lý tên miền ở VN là VNNIC, thế giới là ICANN.
- Sản phẩm hosting của VietNix: Web hosting, seo hosting, email hosting.

## Virtual Private Server - VPS:
- VPS được tạo ra bằng cách chia nhỏ một máy chủ thật thành nhiều máy chủ ảo có tính năng tương tự như máy chủ thật.
- Có 2 công nghệ ảo hóa phổ biến:
    - Ảo hóa cấp hệ điều hành (container-based virtualization): các vps sẽ dùng chung nhân hệ điều hành.
        - Ưu điểm: hiệu suất cao, nhẹ, tốc độ nhanh, tiết kiệm tài nguyên.
        - Nhược điểm: Không thể chạy hệ điều hành khác với máy chủ.
    - Ảo hóa phần cứng (Full/Para virtualization): Mỗi máy chủ ảo sẽ có hệ điều hành riêng.
        - Ưu điểm: Chạy được các hđh khác nhau, cách ly các máy chủ tốt hơn, tăng bảo mật.
        - Nhược điểm: Tiêu tốn tài nguyên hơn container.
## Dedicated Server
- Dedicated server là một máy chủ chạy trên nền tảng của một máy chủ vật lý.
- Dedicated server được đặt tại các datacenter, nơi mà đảm bảo khả năng mạng, báo cháy, điện, điện dự phòng tốt nhất có thể.
- Datatransfer là lượng dữ liệu có thể truyền được giữa vps, server và các thiết bị kết nói với nó trong một khoảng thời gian cụ thể.
- Uptime là thời gian sẵn sàng sử dụng, không bị gián đoạn của vps, server.

## Colocation
- Là dịch vụ cung cấp không gian vật lý trên máy chủ và tài nguyên mạng trong một trung tâm dữ liệu.

## Tối ưu tốc độ web (PageSpeed)
## Firewall anti DDoS
## Đăng ký tên miền và SSL

# Một số kiến thức về phần cứng
## CPU
- Core: Core là đơn vị xử lý độc lập trong CPU, có thể thực hiện các tác vụ một cách riêng biệt. Một CPU có nhiều core có thể xử lý nhiều tác vụ cùng lúc (đa nhiệm - multitasking).
- Thread (luồng) là một đơn vị cơ bản của xử lý trong một tiến trình. Một tiến trình có thể chứa nhiều luồng, và mỗi luồng có thể thực hiện một nhiệm vụ cụ thể.
- Xung nhịp: là tốc độ xử lý của bộ vi xử lý (CPU), đo bằng đơn vị GHz (Gigahertz) hoặc MHz (Megahertz).
- Ram: là bộ nhớ trong của máy tính, lưu trữ dữ liệu tạm thời và có tốc độ truy cập nhanh. Tốc độ Ram được đo bằng Mem Clock (bus) độ trễ (cas).
- Disk: hdd, sdd, nvme.
- RAID: có thể tăng tốc độ truy cập dữ liệu bằng cách phân chia và phân phối dữ liệu trên nhiều ổ đĩa, có tính năng dự phòng redundancy, cho phép kết hợp nhiều ổ đĩa.
    - RAID 0: phân chia dữ liệu thành các phần nhỏ và lưu trên nhiều ổ đĩa.
    - RAID 1: tạo một bản sao dữ liệu lưu trên ổ đĩa khác.
    - RAID 10: kết hợp giữa RAID 0 và RAID 1. Dữ liệu được sao lưu trên nhiều ổ đĩa theo kiểu đồng thời (striping) và dự phòng (mirroring).
- Địa chỉ IP: dùng để kết nối các máy tính lại với nhau.
    - IPv4: gồm 4 số, mỗi số có giá trị từ 0 - 255.
    - IPv6: gồm 8 số, mỗi số có giá trị từ 0 - 65535.
- Port: là một con số từ 0 đến 65535 map với một ứng dụng đang chạy trên máy tính:
    - Port 80: dùng cho http (port 443 giống port 80 nhưng dữ liệu được mã hóa https).
    - Port 25: SMTP.
    - Port 21: FTP.
    - Port 22: SSH.
    - Port 3389: Remort Desktop.
    - Port 2222: direct admin panel.
    - Port 7800: aaPanel.
    - Port 2087/2083: WHM/Cpanel.
- Ở VietNix hiện tại Intel Xeon Platinum là mạnh nhất.
# WebPanel

## Server Control Panel:
- Giúp cài đặt, quản lý các phần mềm, quản lý tệp, quản lý domain, quản lý CSDL, bảo mật: quản lý SSL/TLS & SSH, Monitor, Stats, Logs.

## Direct Admin

## aaPanel

## cPanel




