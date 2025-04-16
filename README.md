🏥 Thiết kế mạng máy tính bệnh viện bằng Cisco Packet Tracer
Dự án này mô phỏng và thiết kế hệ thống mạng nội bộ cho một bệnh viện quy mô vừa, sử dụng phần mềm Cisco Packet Tracer. Mạng được triển khai theo mô hình chuẩn OSI 7 lớp, đảm bảo khả năng phân chia mạng hợp lý, bảo mật, khả năng mở rộng và hiệu suất truyền tải cao.

📚 Mục tiêu
Thiết kế hệ thống mạng LAN/WAN cho bệnh viện

Đảm bảo phân tách mạng cho các phòng ban: Kế toán, Bác sĩ, Điều dưỡng, Hành chính, Phòng lưu trữ...

Triển khai định tuyến (routing), VLAN, DHCP, NAT, và mô phỏng giao tiếp giữa các lớp trong mô hình OSI

Kiểm thử kết nối và truyền thông tin giữa các thiết bị mạng

🧱 Mô hình OSI được áp dụng

Lớp OSI	Thành phần mô phỏng trong dự án
1. Physical	Cáp mạng (copper straight-through, crossover), cổng kết nối
2. Data Link	Switch, địa chỉ MAC, VLAN tagging
3. Network	Router, IP Addressing, Routing Protocol (RIP, OSPF)
4. Transport	TCP/UDP (mô phỏng qua kiểm tra dịch vụ Telnet, FTP, HTTP)
5. Session	Phiên làm việc giữa client-server qua dịch vụ Telnet, SSH
6. Presentation	Mã hóa/giải mã (minh họa ứng dụng gửi dữ liệu định dạng)
7. Application	Giao tiếp giữa người dùng với dịch vụ như HTTP, DNS, FTP
🖥️ Công cụ sử dụng
Cisco Packet Tracer 8.x

Giao thức định tuyến: RIP, OSPF (nếu cần mở rộng)

Mô hình phân vùng mạng: VLAN

Cấu hình DHCP, NAT

Firewall Access Control List (ACL) (nâng cao)

🏗️ Topology mạng (Mô tả tổng quan)
less
Sao chép
Chỉnh sửa
                            [ Internet ]
                                 |
                              [Router]
                                 |
               -----------------+------------------
               |                |                 |
           [Switch]         [Switch]          [Switch]
           (VLAN 10)         (VLAN 20)         (VLAN 30)
             |                  |                 |
       [Phòng bác sĩ]     [Phòng kế toán]    [Phòng điều dưỡng]
Ngoài ra có thể có VLAN riêng cho:

Phòng quản trị hệ thống

Phòng y tế lưu trữ hồ sơ

Guest Wi-Fi cho bệnh nhân

⚙️ Các thành phần chính
Router: Phân chia mạng, cấp route giữa các VLAN/subnet

Switch (Layer 2): Kết nối máy tính nội bộ theo từng phòng ban

PC, Laptop: Mỗi phòng từ 2–5 thiết bị

Server: DNS, Web, FTP đặt tại trung tâm dữ liệu

Firewall (mô phỏng bằng ACL): Hạn chế truy cập giữa các VLAN

📄 Hướng dẫn sử dụng
Mở file .pkt bằng Cisco Packet Tracer

Kiểm tra sơ đồ kết nối và đảm bảo tất cả thiết bị đã có IP đúng subnet

Kiểm thử kết nối bằng công cụ ping, web browser, telnet...

Xem chi tiết cấu hình bằng cách click vào router/switch → tab CLI

🔐 An ninh mạng đề xuất
Sử dụng VLAN để tách mạng theo chức năng

ACL chặn truy cập trái phép giữa các VLAN

SSH thay thế Telnet cho truy cập từ xa

NAT và firewall để kiểm soát truy cập ra/vào Internet

