# Memo quyết định: Trợ lý AI tra cứu tài liệu nội bộ

**Tác giả:** ⏳ (bài cá nhân) · **Ngày:** 14/10/2026 · **Người nhận:** Sponsor (quản lý vận hành) ⏳ · **Chi tiết:** [dashboard-hanh-dong-ai-v2.md](dashboard-hanh-dong-ai-v2.md)

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
| **61–90** Đo giá trị, quyết định | Sponsor + Chủ quy trình | Tiếp tục / sửa / dừng theo quy tắc dưới |

Ba thay đổi bắt buộc: **nguồn kiểm chứng** (nguồn + ngày cập nhật), **người chịu trách nhiệm** (data owner, trưởng ca), **cách xử lý khi AI không chắc** (nói "chưa chắc" và chuyển người).

## Đo gì để quyết định

| Chỉ số | Loại | Mốc đầu | Mục tiêu *(đề xuất)* | Nguồn · Phụ trách | Khi xấu |
| --- | --- | --- | --- | --- | --- |
| Tỷ lệ câu trả lời có nguồn kiểm chứng được (P1) | Product | Phiếu bằng chứng: chấm 20 câu hỏi thật | ≥ 90% | Phiếu chấm mẫu · Chủ quy trình (vai QA) | < 80% hai tuần liền: dừng mở rộng, sửa trong 5 ngày làm việc |
| Tỷ lệ trả lời đúng và đúng phiên bản (P2) | Product | Cùng 20 câu | ≥ 90% | Phiếu chấm mẫu · Chủ quy trình (vai QA) | Lỗi sai nghiêm trọng: ẩn tài liệu đó ngay, sửa trong 2 ngày làm việc |
| Thời gian một lượt tra cứu, median (W1) | Workflow | Bấm giờ cặp 10 câu: thủ công vs qua trợ lý | Giảm ≥ 30% | Phiếu bấm giờ · Chủ quy trình | Không giảm sau 4 tuần: quan sát 5 lượt, sửa cách làm |
| Tỷ lệ lượt phải quay lại tìm thủ công hoặc hỏi người (W2) | Workflow | Phiếu, 20 câu | Giảm ≥ 15 điểm % | Phiếu · Chủ quy trình | Không giảm: bắt buộc mở nguồn, chấm 100% mẫu trong tuần |

Chưa đo được, cần dữ liệu khi triển khai thật và **chưa đặt mục tiêu**: kết quả nghiệp vụ (B1), tỷ lệ đi đúng bước chuẩn (W3), tỷ lệ báo lỗi xử lý đúng hạn (P3). Login và số câu hỏi vẫn theo dõi nhưng **không** dùng để quyết định. Chi tiết ở mục 6 của dashboard.

## Thay đổi từ v1 sau kiểm tra chéo

1. **Ngưỡng và hành động cụ thể:** bỏ "mục tiêu nhóm / tăng kiểm soát" chung chung; mỗi chỉ số có ngưỡng kích hoạt, hành động, người làm, thời hạn.
2. **Gate theo bằng chứng, không theo lượt dùng:** hạ "mức dùng" xuống chỉ số bối cảnh; qua gate dựa trên chất lượng, hành vi và kết quả nghiệp vụ.
3. **Đối chứng và số liệu đo được:** thay thời gian tự khai bằng median từ bấm giờ hoặc log, so với cách thủ công (đo một mình) hoặc ca đối chứng (khi triển khai thật).
4. **TO-BE đổi cách chia việc:** thêm chia việc người–AI (Mollick) và chuỗi tin cậy có owner, thay vì chỉ chèn bước "hỏi AI".

*Lưu ý: bốn thay đổi trên đến từ phản biện theo bốn trục của đề; góp ý của người phản biện thật điền ở mục 7.3 của dashboard.*

## Quy tắc tại ngày 90

- **Tiếp tục / mở rộng:** P1, P2, W1, W2 đạt mục tiêu; kết quả nghiệp vụ (B1) **đã đo** và tốt hơn đối chứng 4 tuần liền; không còn lỗi sai nghiêm trọng. Chưa có B1 thì chưa ra quyết định này.
- **Sửa:** chất lượng chưa đạt nhưng nguyên nhân đã rõ và còn một vòng sửa; hoặc chưa đo được B1.
- **Dừng:** sau hai vòng sửa chất lượng vẫn không đạt, kết quả nghiệp vụ xấu hơn đối chứng, hoặc chi phí vận hành lớn hơn giá trị đo được.

## Cần từ Sponsor

1. Chỉ định **data owner** cho từng tài liệu trong phạm vi và **Phụ trách AI**.
2. Cho phép truy cập **log tác vụ, log QA và dữ liệu nghiệp vụ** (để đo B1, W3, P3), và cho một ca làm **nhóm đối chứng**.
3. Xác nhận ngân sách và người vận hành cho giai đoạn 0–30. ⏳
