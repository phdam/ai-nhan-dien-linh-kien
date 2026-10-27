# AI Nhận Diện Linh Kiện — bản Gemini ưu tiên miễn phí

## Tính năng
- Giao diện tiếng Việt, tối ưu điện thoại.
- Chọn nhiều ảnh hoặc chụp ảnh; chọn video và trích tối đa 4 khung hình.
- Gửi ảnh thật tới Gemini API; bật Google Search grounding để tìm thông tin/datasheet khi công cụ khả dụng.
- API key chỉ lưu ở biến môi trường máy chủ, không nhúng vào HTML.

## Lưu ý miễn phí
Gemini API có hạn mức miễn phí cho một số model/tài khoản, nhưng không bảo đảm mọi model/tính năng đều miễn phí hoặc không giới hạn. Mặc định dùng `gemini-2.5-flash`; hãy kiểm tra model và hạn mức hiện tại trong Google AI Studio. Không bật thanh toán nếu muốn giữ mức 0 đồng.

## Chạy trên máy tính
Cần Node.js 20+. Trong thư mục này, đặt biến môi trường `GEMINI_API_KEY` bằng khóa bí mật của bạn rồi chạy `npm start`.
- Windows PowerShell: `$env:GEMINI_API_KEY="YOUR_KEY"; npm start`
- macOS/Linux: `export GEMINI_API_KEY="YOUR_KEY" && npm start`
Mở `http://localhost:3000`.

## Triển khai máy chủ
Đưa toàn bộ thư mục lên nền tảng hỗ trợ Node.js, lệnh chạy `npm start`, đặt biến môi trường `GEMINI_API_KEY` trên trang cấu hình máy chủ và mở URL HTTPS được cấp. Không đặt khóa trong `index.html`, không gửi khóa cho người khác. Gói miễn phí của hosting có thể ngủ hoặc có giới hạn.

## An toàn và giới hạn
Video chỉ được phân tích bằng các khung hình tĩnh, không phân tích tiếng. Hãy xác minh mã/model với tài liệu hãng trước khi mua hoặc đấu nối thiết bị.
