# Memo quyết định: Trợ lý AI tra cứu tài liệu nội bộ

**Nhóm:** ⏳ · **Ngày:** 14/10/2026 · **Người nhận:** Sponsor (quản lý vận hành) ⏳ · **Chi tiết:** [dashboard-hanh-dong-ai-v2.md](dashboard-hanh-dong-ai-v2.md)

## Quyết định: SỬA

Tiếp tục pilot nhỏ để sửa độ tin cậy và quy trình. **Chưa mở rộng**, và không dùng số lượt dùng làm thước đo thành công.

## Phạm vi

Trợ lý AI tra cứu tài liệu nội bộ · nhân viên vận hành · ba quy trình: tra cứu, tóm tắt, kiểm chứng và báo lỗi.

Công cụ đã **deployment** nhưng chưa **adoption**: công việc, trách nhiệm và cách kiểm soát chưa đổi.

## Vì sao: hai nguyên nhân gốc

Triệu chứng là nhân viên vẫn tìm file thủ công. Nguyên nhân:

1. **Độ tin cậy.** Câu trả lời không có nguồn và ngày cập nhật, không có QA mẫu hay cách báo lỗi, nên người dùng không có cơ sở để tin. *(5 câu hỏi, ADKAR tại Desire, Gartner-Lite. Case: Morgan Stanley mở rộng sau khi có khung đánh giá.)*
2. **Workflow và chia việc.** Trợ lý nằm ngoài bước tra cứu chính thức; chưa rõ ai kiểm chứng, ai chịu trách nhiệm, chuyển người ở đâu. *(5 câu hỏi, Mollick, Gartner-Lite tại Absorption. Case: Klarna phải tuyển lại người khi chất lượng giảm.)*

Đào tạo một mình không giải được vì điểm nghẽn là Desire: người dùng ngại tin câu trả lời không thấy nguồn. Gartner-Lite cho kết quả hướng đi đạt, dữ liệu/governance/vận hành/hấp thụ thiếu, nên chưa rollout rộng.

## Làm gì: lộ trình 30–60–90

| Giai đoạn | Owner | Gate để sang bước sau |
| --- | --- | --- |
| **0–30** Nền tin cậy | Phụ trách AI + Data owner | Mọi tài liệu có owner và lịch cập nhật; có mốc đầu đủ; kênh báo lỗi chạy; ≥1 vòng QA mẫu |
| **31–60** Pilot trong workflow | Chủ quy trình | Tỷ lệ có nguồn và đúng đạt mục tiêu; thời gian giảm so với mốc đầu **và** nhóm đối chứng; chất lượng và kết quả nghiệp vụ không xấu đi |
| **61–90** Đo giá trị, quyết định | Sponsor + Chủ nghiệp vụ | Tiếp tục / sửa / dừng theo quy tắc dưới |

Ba thay đổi bắt buộc: **nguồn kiểm chứng** (nguồn + ngày cập nhật), **người chịu trách nhiệm** (data owner, trưởng ca), **cách xử lý khi AI không chắc** (nói "chưa chắc" và chuyển người).

## Đo gì để quyết định

| Chỉ số | Loại | Mốc đầu | Mục tiêu *(đề xuất)* | Nguồn · Phụ trách | Khi xấu |
| --- | --- | --- | --- | --- | --- |
| Tỷ lệ câu trả lời có nguồn kiểm chứng được | Product | Chấm mẫu tuần 1 | ≥ 90% | Chấm mẫu · Phụ trách QA | < 80% hai tuần liền: dừng mở rộng, sửa trong 5 ngày làm việc |
| Thời gian hoàn thành một lượt tra cứu (median) | Workflow | Log + bấm giờ tuần 1 | Giảm ≥ 30% vs mốc đầu và vs đối chứng | Log tác vụ · Chủ quy trình | Không giảm sau 4 tuần: quan sát 5 lượt, sửa cách làm |
| Tỷ lệ lượt hoàn thành không phải làm lại | Workflow | Mẫu hồ sơ ca tuần 1 | +15 điểm % | Log QA rework · Phụ trách QA | Tăng làm lại: bắt buộc mở nguồn, QA 100% mẫu trong tuần |
| Kết quả nghiệp vụ (đúng quy định lần đầu) | Business | Hệ thống nghiệp vụ tuần 1–2 | Tốt hơn đối chứng, không xấu đi | Hệ thống nghiệp vụ · Chủ nghiệp vụ | Xấu hơn đối chứng: thu hẹp phạm vi; dừng nếu 2 vòng sửa không đảo ngược |

Login và số câu hỏi vẫn theo dõi nhưng **không** dùng để quyết định. Thời gian tiết kiệm tự khai chỉ để đối chiếu với số từ log. Bộ đầy đủ (8 chỉ số quyết định, 1 chỉ số bối cảnh) ở dashboard.

## Thay đổi từ v1 sau kiểm tra chéo

1. **Ngưỡng và hành động cụ thể:** bỏ "mục tiêu nhóm / tăng kiểm soát" chung chung; mỗi chỉ số có ngưỡng kích hoạt, hành động, người làm, thời hạn.
2. **Gate theo bằng chứng, không theo lượt dùng:** hạ "mức dùng" xuống chỉ số bối cảnh; qua gate dựa trên chất lượng, hành vi và kết quả nghiệp vụ.
3. **Nhóm đối chứng và số liệu từ log:** thay thời gian tự khai bằng median từ log so với nhóm đối chứng.
4. **TO-BE đổi cách chia việc:** thêm chia việc người–AI (Mollick) và chuỗi tin cậy có owner, thay vì chỉ chèn bước "hỏi AI".

*Lưu ý: bốn thay đổi trên đến từ phản biện theo bốn trục của đề; góp ý của nhóm đổi chéo thật điền ở mục 7.3 của dashboard.*

## Quy tắc tại ngày 90

- **Tiếp tục / mở rộng:** tỷ lệ có nguồn và đúng đạt mục tiêu; hành vi đạt; kết quả nghiệp vụ tốt hơn đối chứng 4 tuần liền; không còn lỗi sai nghiêm trọng.
- **Sửa:** chất lượng chưa đạt nhưng nguyên nhân đã rõ và còn một vòng sửa.
- **Dừng:** sau hai vòng sửa chất lượng vẫn không đạt, kết quả nghiệp vụ xấu hơn đối chứng, hoặc chi phí vận hành lớn hơn giá trị đo được.

## Cần từ Sponsor

1. Chỉ định **data owner** cho từng tài liệu trong phạm vi và **Phụ trách AI**.
2. Cho phép truy cập **log tác vụ và log QA**, và cho một ca làm **nhóm đối chứng**.
3. Xác nhận ngân sách và người vận hành cho giai đoạn 0–30. ⏳
