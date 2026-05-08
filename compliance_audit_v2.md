## Audit Toàn Diện Theo Điều Luật
 
> Áp dụng prompt AI Compliance Officer từ Day 22 vào DOMIN-H Family.
 
---
 
### VI PHẠM 1: Claim chưa có evidence — "Giảm 70% cãi vã"
- **Luật áp dụng:** BLHS Việt Nam
- **Điều:** Điều 198 — Lừa dối khách hàng
- **Bằng chứng trong sản phẩm:** Pitch deck ghi *"Pilot 50 gia đình: Giảm 70% số cuộc cãi vã về tiền bạc"* — số liệu dự kiến được trình bày như đã xảy ra
- **Pattern khớp với:** Vụ kẹo Kera — ghi "28.43% bột rau củ" khi thực tế 0.935%. Cùng pattern: dự kiến viết như fact
- **Hành động sửa:** (1) Xóa % cụ thể, thay bằng "mục tiêu đo lường"; (2) Chỉ dùng số liệu sau khi pilot có data thật; (3) Founder ký file evidence trước khi đưa vào bất kỳ tài liệu marketing nào
- **Deadline:** Trước launch landing page
---
 
### VI PHẠM 2: Xử lý dữ liệu người dùng dưới 18 tuổi
- **Luật áp dụng:** Luật BVDLCN 91/2025/QH15
- **Điều:** Điều 9 — Dữ liệu cá nhân nhạy cảm của trẻ em; Điều 30 — Điều kiện xử lý
- **Bằng chứng trong sản phẩm:** PRD xác định đối tượng là sinh viên ĐH — một số có thể dưới 18 tuổi. App thu thập hóa đơn + thói quen chi tiêu của nhóm này mà không có cơ chế xác minh độ tuổi
- **Pattern khớp với:** Vụ rò rỉ CIC — xử lý dữ liệu cá nhân thiếu kiểm soát → PDPL Điều 8 & 30
- **Hành động sửa:** (1) Thêm xác minh tuổi khi đăng ký; (2) Với user dưới 18: yêu cầu consent phụ huynh; (3) Không dùng dữ liệu người dưới 18 để train model
- **Deadline:** 60 ngày sau khi launch (DPIA)
---
 
### VI PHẠM 3: Privacy Policy thiếu hoặc không đúng PDPL
- **Luật áp dụng:** Luật BVDLCN 91/2025/QH15
- **Điều:** Điều 16 — Thông báo xử lý dữ liệu; Điều 30 — Đăng ký với Bộ Công an
- **Bằng chứng trong sản phẩm:** PRD không đề cập Privacy Policy. App xử lý ảnh hóa đơn (dữ liệu tài chính), thói quen chi tiêu (dữ liệu hành vi) nhưng chưa có cơ chế thông báo theo PDPL
- **Pattern khớp với:** Vụ rò rỉ CIC — PDPL phạt 10x doanh thu
- **Hành động sửa:** (1) Viết Privacy Policy tiếng Việt; (2) Đăng ký xử lý dữ liệu với Bộ Công an trước launch; (3) Thêm màn hình consent rõ ràng khi onboarding
- **Deadline:** Trước launch (bắt buộc)
---
 
### VI PHẠM 4: AI "phán xử" tài chính chưa phân loại rủi ro
- **Luật áp dụng:** Luật AI VN 134/2025/QH15
- **Điều:** Điều 9 — Phân loại hệ thống AI theo mức độ rủi ro
- **Bằng chứng trong sản phẩm:** Tính năng Smart Request — "AI tự động quét giá thị trường thẩm định → Bố mẹ duyệt 1 chạm" và Red Flag Alerts "phát hiện chi tiêu rủi ro" — ảnh hưởng trực tiếp quan hệ gia đình và quyết định tài chính
- **Pattern khớp với:** Luật AI VN mới hiệu lực 1/3/2026 — chưa có vụ enforcement nhưng cần tuân thủ ngay
- **Hành động sửa:** (1) Tự phân loại: Smart Request + Red Flag = medium-high risk; (2) Thông báo Bộ KH&CN; (3) Thêm disclaimer trong app "AI chỉ đưa gợi ý, không thay thế quyết định của phụ huynh"
- **Deadline:** Trước launch commercial
---
 
### VI PHẠM 5: Sử dụng Gemini (Google) — Chưa kiểm tra đại diện pháp lý VN
- **Luật áp dụng:** Luật BVDLCN 91/2025/QH15
- **Điều:** Điều 14 — Chuyển dữ liệu ra nước ngoài
- **Bằng chứng trong sản phẩm:** PRD ghi *"Model: Gemini 1.5 Flash"* — ảnh hóa đơn (dữ liệu tài chính) được gửi lên server Google để OCR → chuyển dữ liệu cá nhân ra nước ngoài
- **Pattern khớp với:** Vụ rò rỉ CIC — "Engineer paste data lên ChatGPT công cộng" → PDPL Điều 8
- **Hành động sửa:** (1) Kiểm tra Google Cloud có đại diện pháp lý VN chưa; (2) Ký DPA (Data Processing Agreement) với Google; (3) Thêm điều khoản trong ToS về việc dữ liệu được xử lý bởi Google AI
- **Deadline:** Trước launch
---
 
### VI PHẠM 6: Không có cơ chế Abuse Monitoring cho Red Flag
- **Luật áp dụng:** BLHS VN
- **Điều:** Điều 324 — Rửa tiền (pattern Pips: biết dấu hiệu vẫn process)
- **Bằng chứng trong sản phẩm:** App xử lý giao dịch tiền giữa phụ huynh và sinh viên. Nếu có người dùng lợi dụng app để chuyển tiền bất hợp pháp (VD: sinh viên làm "người nhận" trong sơ đồ lừa đảo) và app có dấu hiệu bất thường nhưng không báo cáo → rủi ro Điều 324
- **Pattern khớp với:** Vụ Mr Pips / Shark Bình — "biết dấu hiệu phạm tội, vẫn tiếp tục vận hành hệ thống"
- **Hành động sửa:** (1) Xây dựng abuse report flow; (2) Log các giao dịch bất thường (amount >5 triệu đột xuất, pattern lạ); (3) Có quy trình escalation khi phát hiện dấu hiệu vi phạm
- **Deadline:** Trước launch
---
 
### VI PHẠM 7: "Private Mode" che giấu thông tin — Xung đột quyền lợi pháp lý
- **Luật áp dụng:** Luật BVDLCN 91/2025/QH15 + Luật Hôn nhân Gia đình
- **Điều:** Điều 9 PDPL — Dữ liệu nhạy cảm; Quyền riêng tư cá nhân
- **Bằng chứng trong sản phẩm:** Tính năng Private Mode: *"AI chỉ báo cáo tổng tiền mục cá nhân nhạy cảm, không báo chi tiết"* — có thể xung đột giữa quyền riêng tư của sinh viên (người dùng) vs quyền giám sát của phụ huynh (người trả tiền)
- **Pattern khớp với:** Mới — chưa có vụ VN nhưng là rủi ro tiềm ẩn nếu sinh viên kiện về quyền riêng tư
- **Hành động sửa:** (1) Tư vấn luật sư về ranh giới giám sát tài chính vs quyền riêng tư; (2) Thêm consent rõ ràng từ sinh viên về những gì phụ huynh thấy; (3) Tuổi 18+ có quyền từ chối tính năng Private Mode tracking
- **Deadline:** Trước launch
---
 
### TOP 5 VI PHẠM NGHIÊM TRỌNG NHẤT:
 
| Thứ tự | Vi phạm | Mức độ | 3 Hành động sửa |
|--------|---------|--------|-----------------|
| 1 | Privacy Policy + đăng ký PDPL | 🔴 Cực cao | (1) Viết PP tiếng Việt; (2) Đăng ký Bộ Công an; (3) Thêm consent screen |
| 2 | Claim "70% giảm cãi vã" | 🔴 Cực cao | (1) Xóa % cụ thể; (2) Chỉ publish sau pilot; (3) Founder ký evidence |
| 3 | Chuyển dữ liệu ra nước ngoài (Gemini) | 🟠 Cao | (1) Ký DPA với Google; (2) Thêm điều khoản ToS; (3) Cân nhắc edge processing |
| 4 | Phân loại rủi ro AI Điều 9 | 🟠 Cao | (1) Self-classify; (2) Thông báo Bộ KH&CN; (3) Thêm AI disclaimer |
| 5 | Không có Abuse Monitoring | 🟡 Trung bình | (1) Build abuse report; (2) Log giao dịch bất thường; (3) Escalation policy |
 
---
