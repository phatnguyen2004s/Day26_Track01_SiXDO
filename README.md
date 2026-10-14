# Day26_Track01_SiXDO

Bài thực hành tổng hợp Day 26: **dashboard hành động cho áp dụng AI (v2) kèm memo quyết định**. Sản phẩm: trợ lý AI tra cứu tài liệu nội bộ (tình huống minh hoạ của đề, làm cá nhân, chưa có số đo thật).

## 1. Thành viên

| Họ tên | MSSV | Phần phụ trách | Góp ý đã đưa cho nhóm bạn |
| --- | --- | --- | --- |
| Nguyễn Tiến Phát | 2A202602387 | Toàn bộ bài (làm cá nhân): phạm vi, chẩn đoán, workflow, lộ trình 30–60–90, dashboard, memo | ⏳ *Chưa điền: nhóm/bạn đã phản biện và 2 góp ý cụ thể* |

**Người phản biện bài này:** bạn Tiến (4 trục: phạm vi, framework, chỉ số, hành động). Chi tiết ở sheet "Kiểm tra chéo" trong [`dashboard/dashboard_hanh_dong_v2.xlsx`](dashboard/dashboard_hanh_dong_v2.xlsx).

## 2. Phạm vi

1 sản phẩm AI (trợ lý tra cứu tài liệu nội bộ) · 1 nhóm người dùng chính (nhân viên vận hành) · 3 quy trình (Q1 tra cứu, Q2 tóm tắt, Q3 kiểm chứng và báo lỗi). Vấn đề: nhân viên vẫn quay lại tìm file thủ công.

## 3. Nguyên nhân gốc

1. **Độ tin cậy** (5 câu hỏi, ADKAR): câu trả lời không nguồn, không QA mẫu, không cách báo lỗi.
2. **Workflow và chia việc** (5 câu hỏi, Mollick): trợ lý nằm ngoài bước tra cứu chính thức, chưa rõ ai kiểm chứng.

Gartner-Lite chỉ đánh giá readiness (pilot nhỏ, chưa rollout rộng). Bằng chứng: case tham khảo Morgan Stanley, Klarna, DWP/GDS (loại: case công bố, nguồn ở sheet "Nguồn"); phép thử hiện trường là kế hoạch, chưa thực hiện.

## 4. Cách làm mới

Ba thay đổi bắt buộc: **nguồn kiểm chứng** (nguồn + ngày cập nhật) · **người chịu trách nhiệm** (data owner, trưởng ca) · **cách xử lý khi AI không chắc** (nói "chưa chắc" và chuyển người). Lộ trình 30–60–90 có owner và gate từng giai đoạn.

## 5. Chỉ số

- **P1** (Product): mốc đầu: Tuần 1: chấm 20 câu hỏi (cột 'Nguồn mở được và còn hiệu lực') · mục tiêu: ≥ 90% tại Gate 2 (đề xuất) · nguồn: Phiếu chấm mẫu; về sau bộ câu hỏi vàng + chấm hằng tuần · owner: Chủ quy trình (vai QA)
- **W1** (Workflow Q1): mốc đầu: Tuần 1: bấm giờ cặp 10 câu, cách thủ công vs qua trợ lý · mục tiêu: Giảm ≥ 30% so với cách thủ công, và so với ca đối chứng khi có (đề xuất) · nguồn: Phiếu bấm giờ; về sau log tác vụ · owner: Chủ quy trình
- **W2** (Workflow Q1–Q2): mốc đầu: Tuần 1: cột 'Phải tìm lại hoặc hỏi người', 20 câu · mục tiêu: Giảm ≥ 15 điểm % so với mốc đầu (đề xuất) · nguồn: Phiếu; về sau log QA / ticket mở lại · owner: Chủ quy trình

Còn P2 (tỷ lệ đúng) và các chỉ số cần dữ liệu thật (B1, W3, P3); mỗi chỉ số kèm hành động khi xấu, xem sheet "Chỉ số".

## 6. Quyết định

**SỬA** (tiếp tục pilot nhỏ, chưa mở rộng): đã có hai nguyên nhân gốc nhưng chưa có B1 để chứng minh giá trị nghiệp vụ.
Hai thay đổi chính so với v1: (1) tiêu chí hoàn thành cho "tóm tắt" và làm rõ Gartner-Lite chỉ là readiness; (2) mốc đầu B1 và quyền dữ liệu phải có từ Gate 1 (ngày 30).

## Cấu trúc repo

```
Day26_Track01_SiXDO/
├── README.md
├── dashboard/dashboard_hanh_dong_v2.xlsx   ← bản v2 sau kiểm tra chéo
├── memo/memo_quyet_dinh.md                 ← memo 5 phần
└── v1/dashboard_hanh_dong_v1.xlsx          ← bản trước phản biện, để đối chiếu
```
