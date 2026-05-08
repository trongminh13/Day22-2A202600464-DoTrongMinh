## Phạm Vi Lãnh Thổ & Luật Áp Dụng
 
### Câu hỏi 1: Luật nào áp dụng chính?
 
**Trả lời:** DOMIN-H Family là sản phẩm B2C, server và người dùng tại Việt Nam → áp dụng đồng thời:
 
| Luật | Áp dụng vì | Mức độ |
|------|-----------|--------|
| **Luật AI VN 134/2025/QH15** (hiệu lực 1/3/2026) | App sử dụng AI phân tích dữ liệu tài chính cá nhân → thuộc phạm vi | **Bắt buộc** |
| **Luật BVDLCN 91/2025/QH15** (hiệu lực 1/1/2026) | Xử lý dữ liệu hóa đơn + thói quen chi tiêu của người dùng dưới 18 tuổi | **Bắt buộc** |
| **BLHS VN — Điều 198** | Nếu claim marketing không có evidence → Lừa dối khách hàng | **Rủi ro hình sự** |
| **EU AI Act** | Nếu có user tại EU hoặc gọi vốn từ quỹ EU-based | Tham khảo |
 
### Câu hỏi 2: App có xử lý dữ liệu người dùng dưới 18 tuổi không?
 
**Trả lời: CÓ** — Sinh viên năm nhất có thể dưới 18 tuổi. Đây là **dữ liệu nhạy cảm** theo PDPL Điều 9. Cần:
- Consent riêng từ phụ huynh (không chỉ từ sinh viên)
- Không dùng dữ liệu của người dưới 18 tuổi để train model
### Câu hỏi 3: AI phân loại tầng rủi ro theo Điều 9 Luật AI VN?
 
| Tính năng | Tầng rủi ro | Lý do |
|-----------|------------|-------|
| OCR hóa đơn | **Thấp** | Xử lý ảnh, không ảnh hưởng quyết định quan trọng |
| AI thẩm định giá thị trường | **Trung bình** | Ảnh hưởng quyết định tài chính gia đình |
| Red Flag Alerts | **Trung bình-Cao** | Có thể gây hậu quả xã hội (mâu thuẫn gia đình, tâm lý sinh viên) |
| Smart Request (AI phán xử) | **Trung bình-Cao** | Ảnh hưởng trực tiếp đến mối quan hệ gia đình + quyết định tài chính |
 
→ **Kết luận:** Cần thông báo Bộ KH&CN (medium risk) trước khi launch commercial.
 
### 4 Deadline Quan Trọng:
 
| # | Deadline | Hành động | Luật |
|---|----------|-----------|------|
| D1 | **Trước launch** | Đăng ký xử lý dữ liệu cá nhân với Bộ Công an | PDPL Điều 30 |
| D2 | **Trước launch** | Update Privacy Policy theo PDPL — cần có tiếng Việt | PDPL Điều 16 |
| D3 | **60 ngày sau khi xử lý dữ liệu nhạy cảm** | Nộp DPIA (Data Protection Impact Assessment) | PDPL Điều 30 |
| D4 | **Trước khi marketing campaign** | Founder ký phê duyệt mỗi claim → có file evidence đính kèm | Điều 198 BLHS |
 
---
