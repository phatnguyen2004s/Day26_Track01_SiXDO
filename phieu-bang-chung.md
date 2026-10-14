# Phiếu đo mốc đầu (kế hoạch, chưa thực hiện)

Phiếu này là công cụ đo mốc đầu của **P1, P2, W1, W2** và kiểm tra hai nguyên nhân gốc (mục 3.5 và 6A của [dashboard](dashboard-hanh-dong-ai-v2.md)). Người đo chỉ cần tick `Y`/`N` và gõ số giây (khoảng 30–45 phút).

> **Trạng thái:** bài tập này dựa trên ví dụ của đề, không có công cụ AI hay tài liệu nội bộ thật, nên **phiếu chưa được điền và 20 câu hỏi bên dưới chỉ là bộ mẫu.** Phiếu sẽ được làm ở tuần 1 của pilot thật (Gate 1). Không điền số giả vào phiếu.

## Cách làm

1. Phiếu đã có sẵn **20 câu hỏi mẫu** (10 câu đầu là tra cứu một đáp án rõ để bấm giờ; 10 câu sau gồm chính sách, biểu mẫu, tóm tắt). **Khi triển khai thật, thay bằng câu hỏi thật của đơn vị** (mẫu thay ở cuối phiếu). Câu mà tài liệu nội bộ không có đáp án thì không đo được độ tin cậy của trợ lý.
2. Với mỗi câu, hỏi trợ lý và điền các cột `Y`/`N`.
3. Với **10 câu đầu (⏱)**, bấm giờ **cả hai cách** trên cùng câu hỏi: tìm thủ công (thư mục, hỏi người) và hỏi trợ lý rồi mở nguồn kiểm tra.
   - Câu **lẻ** (1, 3, 5, 7, 9): làm *thủ công trước*. Câu **chẵn** (2, 4, 6, 8, 10): làm *trợ lý trước*. Mục đích là bù lệch do lần làm sau đã biết đáp án.
4. "Đúng" nghĩa là khớp với bản tài liệu chính thức hiện hành. Không chắc thì ghi `N`. Với câu tóm tắt (ví dụ câu 16, 17, 20), "đúng" là bản tóm tắt có đủ các mục bắt buộc (điều kiện áp dụng, ngoại lệ, hạn/hiệu lực, người phê duyệt) và không thêm nội dung không có trong nguồn (tiêu chí Q2 ở mục 1 của dashboard).

## Phần A. Chấm 20 câu hỏi

| # | Câu hỏi (ghi tắt) | Có nguồn? | Có ngày cập nhật? | Nguồn mở được **và** còn hiệu lực? | Nội dung đúng? | Phải tìm lại hoặc hỏi người sau đó? | ⏱ Thủ công (giây) | ⏱ Trợ lý + mở nguồn (giây) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Quy trình xử lý yêu cầu hoàn tiền của khách gồm những bước nào? | | | | | | | |
| 2 | Yêu cầu hoàn tiền vượt mức nào thì phải có cấp trên phê duyệt? | | | | | | | |
| 3 | Thời hạn xử lý tối đa của một ca khiếu nại là bao lâu? | | | | | | | |
| 4 | Khi hệ thống ngừng hoạt động thì báo cho ai trước? | | | | | | | |
| 5 | Điều kiện để leo thang một ca lên cấp quản lý là gì? | | | | | | | |
| 6 | Biểu mẫu nào dùng để đề nghị cấp lại quyền truy cập hệ thống? | | | | | | | |
| 7 | Ai là đầu mối xử lý các ca liên quan đến dữ liệu khách hàng? | | | | | | | |
| 8 | Lịch nộp báo cáo vận hành hằng tuần là khi nào? | | | | | | | |
| 9 | Đề nghị thay đổi thông tin khách hàng cần đính kèm giấy tờ gì? | | | | | | | |
| 10 | Hồ sơ ca phải được lưu trữ trong bao lâu? | | | | | | | |
| 11 | Chính sách bảo mật hiện hành nói gì về việc gửi file khách hàng qua email? | | | | | | — | — |
| 12 | Quy định mới nhất về ca trực cuối tuần có hiệu lực từ ngày nào? | | | | | | — | — |
| 13 | Ai được truy cập hồ sơ khách hàng loại nhạy cảm? | | | | | | — | — |
| 14 | Quy định cũ và mới về xử lý ngoại lệ khác nhau ở đâu? | | | | | | — | — |
| 15 | Mẫu báo cáo sự cố nằm ở đâu và gồm những mục nào? | | | | | | — | — |
| 16 | Tóm tắt tài liệu hướng dẫn xử lý sự cố trong 5 dòng | | | | | | — | — |
| 17 | Quy trình xử lý khiếu nại bản mới thay đổi gì so với bản trước? | | | | | | — | — |
| 18 | Liệt kê các bước trong hướng dẫn bàn giao ca | | | | | | — | — |
| 19 | Phần nào của sổ tay vận hành nói về xử lý ca ngoài giờ? | | | | | | — | — |
| 20 | Những điểm cần lưu ý trong tài liệu hướng dẫn nhân viên mới? | | | | | | — | — |

## Phần B. Quan sát hành vi (người dùng pilot tick một ô mỗi dòng)

**B1. Tôi thường mở trợ lý ở bước nào của công việc?**
- [ ] Mở ngay từ đầu, trước khi tìm file
- [ ] Chỉ mở sau khi tìm thủ công không ra
- [ ] Hầu như không mở

**B2. Sau khi nhận câu trả lời, tôi thường:**
- [ ] Dùng luôn
- [ ] Tìm lại file gốc để chắc chắn
- [ ] Hỏi đồng nghiệp xác nhận

**B3. Lần gần nhất tôi *không* dùng trợ lý, lý do chính là:**
- [ ] Không biết có tin được câu trả lời không
- [ ] Không thấy nguồn hoặc ngày cập nhật
- [ ] Lần trước nó trả lời sai
- [ ] Quên, hoặc không nghĩ đến
- [ ] Chậm hơn tự tìm
- [ ] Không biết hỏi kiểu gì
- [ ] Lý do khác: ______

## Phần C. Tổng hợp (tính từ phần A)

| Chỉ số | Cách tính | Kết quả |
| --- | --- | --- |
| **P1** Tỷ lệ có nguồn kiểm chứng được | số dòng `Y` ở cột "Nguồn mở được và còn hiệu lực" ÷ 20 | ____ % |
| **P2** Tỷ lệ đúng | số dòng `Y` ở cột "Nội dung đúng" ÷ 20 | ____ % |
| **W2** Tỷ lệ phải quay lại tìm hoặc hỏi người | số dòng `Y` ở cột "Phải tìm lại hoặc hỏi người" ÷ 20 | ____ % |
| **W1** Thời gian thủ công (median) | median cột "⏱ Thủ công", 10 câu đầu | ____ giây |
| **W1** Thời gian qua trợ lý (median) | median cột "⏱ Trợ lý + mở nguồn", 10 câu đầu | ____ giây |
| Mức giảm W1 | 1 − (qua trợ lý ÷ thủ công) | ____ % |

## Cách đọc nhanh (ngưỡng đề xuất, để khỏi chọn bằng chứng theo ý mình)

| Nếu thấy... | thì... |
| --- | --- |
| P1 hoặc P2 dưới 80% | **RC1 (độ tin cậy) được ủng hộ** |
| P1 và P2 đều từ 90% mà W2 vẫn trên 30%, hoặc B3 chủ yếu là "không biết hỏi kiểu gì" / "quên" | **RC1 yếu**; xem lại Awareness/Knowledge trong ADKAR |
| B1 chủ yếu là "chỉ mở sau khi tìm thủ công không ra" hoặc "hầu như không mở" | **RC2 (workflow) được ủng hộ** |
| B1 chủ yếu là "mở ngay từ đầu" | **RC2 yếu**; trợ lý đã nằm trong công việc |

## Hạn chế cần ghi vào bài

- Một người đo, một người chấm: có thể thiên vị. Khi triển khai thật cần 2 người chấm độc lập.
- Mẫu 20 câu (10 câu có bấm giờ) là **mốc đầu**, không đủ để kết luận cho cả tổ chức.
- Cùng một câu làm hai cách thì lần sau nhanh hơn do đã biết đáp án; thứ tự lẻ/chẵn chỉ giảm lệch, không xoá hẳn.

## Mẫu để thay câu hỏi (thay chỗ trong ngoặc bằng việc thật của đơn vị)

| Nhóm | Mẫu câu hỏi |
| --- | --- |
| **Quy trình xử lý ca** (5) | "Quy trình xử lý [loại ca hay gặp] gồm những bước nào?" · "Ca [loại ngoại lệ] cần ai phê duyệt?" · "Thời hạn xử lý tối đa của [loại ca] là bao lâu?" · "Khi [sự cố] xảy ra thì báo ai trước?" · "Điều kiện để leo thang [loại ca] lên cấp trên là gì?" |
| **Chính sách và quy định** (5) | "Chính sách [hoàn tiền/đổi trả/bảo mật] hiện hành nói gì về [tình huống]?" · "Quy định mới nhất về [chủ đề] có hiệu lực từ ngày nào?" · "Ai được truy cập [tài liệu/hệ thống]?" · "Ngưỡng phê duyệt cho [khoản/hạng mục] là bao nhiêu?" · "Quy định cũ và mới về [chủ đề] khác nhau ở đâu?" |
| **Biểu mẫu và đầu mối** (5) | "Biểu mẫu nào dùng cho [việc]?" · "Ai là đầu mối của [mảng việc]?" · "Mẫu báo cáo [loại] nằm ở đâu?" · "Lịch nộp [báo cáo] là khi nào?" · "Cần đính kèm những giấy tờ nào cho [yêu cầu]?" |
| **Tóm tắt** (5) | "Tóm tắt tài liệu [tên] trong 5 dòng" · "Phiên bản mới của [tài liệu] thay đổi gì so với bản cũ?" · "Những điểm cần lưu ý trong [tài liệu dài]?" · "Liệt kê các bước trong [hướng dẫn]" · "Phần nào của [tài liệu] liên quan đến [chủ đề]?" |

## Dùng kết quả thế nào (khi đã triển khai thật)

Điền phần C vào cột "Mốc đầu" ở mục 6A và kết quả vào mục 3.5 của dashboard. Đối chiếu với bảng "Cách đọc nhanh": nếu số liệu bác bỏ giả thuyết thì sửa chẩn đoán ở mục 3.1 và 3.4 chứ không giữ nguyên. Sau đó chỉnh các mục tiêu "(đề xuất)" theo mốc đầu, ví dụ nếu P1 đã gần 95% thì mục tiêu ≥ 90% không còn ý nghĩa.
