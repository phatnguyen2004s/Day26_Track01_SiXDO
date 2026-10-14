# Memo quyết định: Trợ lý AI tra cứu tài liệu nội bộ

**Tác giả:** Nguyễn Tiến Phát (MSSV 2A202602387) · **Ngày:** 14/10/2026 · **Người nhận:** Sponsor (quản lý vận hành) · **Dashboard:** [`dashboard/dashboard_hanh_dong_v2.xlsx`](../dashboard/dashboard_hanh_dong_v2.xlsx)

> Bài tập dựa trên ví dụ xuyên suốt của đề; chưa có số đo thật. Mốc đầu là cách đo sẽ làm ở tuần 1 của pilot.

## 1. Vấn đề và nguyên nhân gốc

Trợ lý đã được cấp phát (deployment) nhưng chưa thành cách làm việc (adoption): nhân viên vận hành vẫn tìm file thủ công hoặc hỏi đồng nghiệp, trong khi dashboard chỉ đếm login và số câu hỏi. Hỏi tiếp "ít dùng vì sao?" thì ra hai nguyên nhân gốc:

1. **Độ tin cậy.** Câu trả lời không có nguồn và ngày cập nhật, không có QA mẫu hay cách báo lỗi, nên người dùng không có cơ sở để tin.
2. **Workflow và chia việc.** Trợ lý nằm ngoài bước tra cứu chính thức; chưa rõ ai kiểm chứng, ai chịu trách nhiệm, chuyển người ở đâu khi AI không chắc.

## 2. Framework đã dùng và bằng chứng

| Nguyên nhân | Framework | Bằng chứng |
| --- | --- | --- |
| RC1 Độ tin cậy | 5 câu hỏi (Tin cậy) · ADKAR (nghẽn ở Desire: ngại tin vì không thấy nguồn) | Case Morgan Stanley: mở rộng sau khi có khung đánh giá. Hiện trường: phép thử 20 câu (kế hoạch, chưa thực hiện) |
| RC2 Workflow | 5 câu hỏi (Workflow) · Mollick (chia việc người–AI) | Case Klarna: khối lượng tự động hoá không thay chất lượng và đường chuyển sang người. Hiện trường: quan sát hành vi (kế hoạch) |

**Gartner-Lite** chỉ dùng để đánh giá readiness (hướng đi đạt; dữ liệu, governance, vận hành, hấp thụ thiếu → pilot nhỏ, chưa rollout rộng). Nó không chứng minh nguyên nhân gốc: hai nguyên nhân trên hiện là giả thuyết có case tham khảo ủng hộ, chờ phép thử xác nhận. Case DWP/GDS dùng cho thiết kế chỉ số (nhóm đối chứng đáng tin hơn tự khai).

## 3. Thay đổi sau phản biện (bạn Tiến)

1. **Phạm vi:** "tóm tắt" giới hạn trong danh mục nguồn ưu tiên và có tiêu chí hoàn thành cho từng quy trình (Q1–Q3).
2. **Framework:** ghi rõ Gartner-Lite chỉ đánh giá readiness; hai nguyên nhân gốc là giả thuyết, chờ phép thử xác nhận.
3. **Chỉ số, hành động:** mốc đầu B1 (kết quả nghiệp vụ) và quyền dữ liệu phải có từ Gate 1 (ngày 30); thiếu thì Sponsor quyết định ngay, không để đến ngày 90.

## 4. Quyết định: SỬA

Tiếp tục pilot nhỏ để sửa độ tin cậy và quy trình trước; chưa mở rộng.

## 5. Lý do, bước tiếp theo và owner

**Lý do:** đã xác định được hai nguyên nhân gốc nhưng chưa có kết quả nghiệp vụ (B1) để chứng minh giá trị, và readiness còn thiếu; chỉ mở rộng khi chất lượng, hiệu quả quy trình và kết quả nghiệp vụ cùng đạt ngưỡng.

| Giai đoạn | Owner | Gate để sang bước sau |
| --- | --- | --- |
| **0–30** Nền tin cậy | Phụ trách AI + Data owner | Mọi tài liệu có owner và lịch cập nhật; mốc đầu P1, P2, W1, W2 và B1 đã ghi; kênh báo lỗi chạy; ≥1 vòng chấm mẫu |
| **31–60** Pilot trong workflow | Chủ quy trình | P1, P2 đạt mục tiêu; W2 và W1 cải thiện so với mốc đầu (và ca đối chứng); không còn lỗi sai nghiêm trọng |
| **61–90** Đo giá trị, quyết định | Sponsor + Chủ quy trình | Tiếp tục / sửa / dừng theo quy tắc dưới |

**Chỉ số quyết định:** P1 (tỷ lệ có nguồn kiểm chứng, mục tiêu ≥ 90%), P2 (tỷ lệ đúng), W1 (thời gian một lượt tra cứu), W2 (tỷ lệ phải quay lại tìm thủ công); đủ mốc đầu, mục tiêu, nguồn, owner, hành động khi xấu ở file dashboard. B1, W3, P3 cần dữ liệu khi triển khai thật.

**Quy tắc tại ngày 90:**
- **Tiếp tục / mở rộng:** P1, P2, W1, W2 đạt mục tiêu; B1 đã đo và tốt hơn đối chứng 4 tuần liền; không còn lỗi sai nghiêm trọng. Chưa có B1 thì chưa ra quyết định này.
- **Sửa:** chất lượng chưa đạt nhưng nguyên nhân đã rõ và còn một vòng sửa; hoặc chưa đo được B1.
- **Dừng:** sau hai vòng sửa chất lượng vẫn không đạt, kết quả nghiệp vụ xấu hơn đối chứng, hoặc chi phí vận hành lớn hơn giá trị đo được.

**Cần từ Sponsor:**
1. Chỉ định data owner cho từng tài liệu trong phạm vi và Phụ trách AI.
2. Cho phép truy cập log tác vụ, log QA và dữ liệu nghiệp vụ (để đo B1, W3, P3) trước Gate 1 (ngày 30), và cho một ca làm nhóm đối chứng.
3. Xác nhận ngân sách và người vận hành cho giai đoạn 0–30.
