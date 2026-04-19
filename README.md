# YOLK_Auto_Daily

================================================================================
          HƯỚNG DẪN CÀI ĐẶT VÀ SỬ DỤNG YOLKGANG TOOL (PHIÊN BẢN V2)
================================================================================

1. YÊU CẦU CÀI ĐẶT THƯ VIỆN (Mở Terminal/CMD và chạy lệnh sau):
--------------------------------------------------------------------------------
npm install axios @solana/web3.js tweetnacl bs58 colors uuid https-proxy-agent node-cron node-machine-id readline

2. CHUẨN BỊ CÁC FILE DỮ LIỆU (Tạo trong cùng thư mục với p2.js):
--------------------------------------------------------------------------------

A. File: privatekey.txt
   - Định dạng: Mỗi dòng là 1 Private Key Solana (Base58).
   - Chức năng: Chứa danh sách ví để chạy tool. 
   - Lưu ý: Tool cố định chỉ chạy tối đa 500 ví đầu tiên trong file này mỗi ngày.

B. File: proxy.txt
   - Định dạng: http://user:pass@ip:port hoặc http://ip:port
   - Chức năng: Đổi IP cho từng ví. Tool sẽ lấy proxy theo thứ tự tương ứng với ví.
   - Định dạng ví dụ: http://proxyuser:proxypass@123.45.67.89:8080

C. File: User_agents.txt
   - Định dạng: Mỗi dòng là 1 chuỗi User Agent trình duyệt.
   - Chức năng: Giả lập thiết bị để tránh bị hệ thống quét.

D. File: license.txt (Tự động tạo)
   - Chức năng: Lưu Key bản quyền sau khi bạn nhập lần đầu. Không cần tự tạo.

3. CÁC TÍNH NĂNG CỐ ĐỊNH TRONG TOOL:
--------------------------------------------------------------------------------
- Threads (Luồng): Cố định 3 luồng chạy song song (Tốc độ tối ưu nhất).
- Limit (Giới hạn): Chỉ chạy 500 tài khoản/ngày để đảm bảo an toàn.
- Reset Day: Tự động Reset vị trí về ví số 1 vào lúc 7:00 sáng mỗi ngày.
- Profile: Tự động lưu UUID và User-Agent cho từng ví vào file 'profiles.json'.

4. QUY TRÌNH LÀM VIỆC CỦA TOOL:
--------------------------------------------------------------------------------
Bước 1: Kiểm tra License (Xác thực HWID máy tính với Server).
Bước 2: Kiểm tra Proxy và lấy IP hiện tại.
Bước 3: Đăng nhập ví bằng chữ ký Solana (Nacl Signature).
Bước 4: Điểm danh hàng ngày (Daily Check-in).
Bước 5: Chơi Crash Game (Ngẫu nhiên 10-20 ván/ngày, chốt lời ở 1.01x).
Bước 6: Quét toàn bộ Task và nhận thưởng (Claim $YOLK & Points).
Bước 7: Nghỉ giải lao (Account Delay) và chuyển sang ví tiếp theo.

5. LỆNH CHẠY TOOL:
--------------------------------------------------------------------------------
node p2

*Lưu ý: Nếu chạy lần đầu, hãy chuẩn bị sẵn Key License để dán vào khi Tool yêu cầu.
================================================================================

Tham Gia NHóm tele : https://t.me/HVchannelss

Tham Gia Discor ( Vip ) : https://discord.gg/gKxvTNu5

Tham gia NHóm VIp Với Chi Phí 1 Tháng 4u - 15u 6thang Lợi ích tham gia nhóm ViP Sẽ được cấp keey sử dụng các tool vip trong discor hỗ trợ Và tham khao Code các tool dự án mà các bạn đề xuất

Gửi Phí tháng vào đây và chụp hình gửi trực tiếp cho tôi tại discor để xác nhận Role VIp ☕ https://huynhviet933.github.io/donate_viet_mmo/ Có thể tặng tôi ít cafe tại đây

Donenat : https://huynhviet933.github.io/donate_viet_mmo/
