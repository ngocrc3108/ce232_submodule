# Giới thiệu
- Mục tiêu chung:
    - Phát triển một hệ thống SMART HOME mang đến trải nghiệm sống tiện nghi, an toàn, tin cậy, bảo mật.
    - Thời gian đáp ứng của hệ thống nhanh chóng dưới 2s.
    - Giao diện người dùng bắt mắt và dễ dàng sử dụng.
- Mục tiêu cụ thể
    - Hệ thống điều khiển đèn tự động.
    - Hệ thống điều khiển quạt và tốc độ quạt.
    - Hệ thống điều khiển cửa tự động.
    - Thiết kế giao diện người dùng thân thiện, dễ sử dụng.
    - Người dùng có thể đăng nhập, đăng ký.
    - Hỗ trợ người dùng thêm mới các thiết bị một cách dễ dàng, thuận tiện.
# Demo
- [Link website](https://ce232-submodule.onrender.com/login).
- [Demo](https://youtu.be/7z1hmoy8tpo) điều khiển các thiết bị, hẹn giờ led.
- [Demo](https://youtu.be/jzDClkvZomQ) tạo tài khoản, đăng nhập, thêm thiết bị.
# Thiết kế kiến trúc hệ thống
![](/images/kien_truc_he_thong.png)\
- ESP32 dùng để điều khiến các thiết bị phần cứng (quạt, đèn, cửa).
- Dùng giao thức MQTT cho giao tiếp giữa backend server và ESP32.
- Có giao diện website tự phát triển cho người dùng thao tác điều khiển từ xa thông qua mạng internet.
- Sử dụng MongoDB lưu trữ dữ liệu của người dùng và các thiết bị có trong hệ thống.
## ESP32
- Sử dụng framework ESP-IDF.
- Dùng module điều khiển động cơ DC L298N để điều khiển tốc độ quạt.
- Điều khiển servo (cửa) bằng điều chế xung (PMW).
- Điều khiển đèn led trực tiếp bằng GPIO.
## Website
- Backend: sử dụng framework Express.js (Node.js) để viết API.
- Fontend: Sử dụng thư viện React kết hợp với Material UI.
- Hosting: Sử dụng dịch vụ hosting miễn phí [render.com](https://render.com/).
![](/images/web.png)
