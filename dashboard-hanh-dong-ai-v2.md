# Dashboard hành động cho áp dụng AI — v2

**Sản phẩm:** Trợ lý AI tra cứu tài liệu nội bộ · **Tác giả:** Nguyễn Tiến Phát (MHV 2A202602387) · bài cá nhân · **Ngày:** 14/10/2026

> **Cách đọc file này**
> - Đây là bài tập dựa trên *ví dụ xuyên suốt của đề* (minh hoạ, không phải số liệu của một doanh nghiệp cụ thể). **Không có công cụ AI hay tài liệu nội bộ thật nào được đo**; các nhận định về hiện trạng lấy từ ví dụ của đề.
> - **Không có số đo thực nào trong file.** Mọi "mốc đầu" là *cách đo + thời điểm đo* sẽ làm ở tuần 1 nếu triển khai thật, không phải con số. Mọi mục tiêu ghi **(đề xuất)** là giá trị khởi điểm, cần xác nhận sau khi có mốc đầu.
> - ⏳ = còn thiếu tên người phản biện (mục 7.3). Danh sách việc còn lại ở mục 10.

---

## 1. Phạm vi đã khoá

| | |
| --- | --- |
| **Sản phẩm AI** | Trợ lý AI tra cứu tài liệu nội bộ (một sản phẩm duy nhất) |
| **Người dùng chính** | Nhân viên vận hành |
| **Quy trình (3)** | **Q1 Tra cứu** quy trình/chính sách khi xử lý một ca · **Q2 Tóm tắt** tài liệu thuộc danh mục nguồn ưu tiên (SOP, chính sách, thông báo thay đổi quy định) cho ca làm việc · **Q3 Kiểm chứng và báo lỗi** nguồn trước khi dùng |
| **Vấn đề quan sát được** | Nhân viên vẫn quay lại tìm file thủ công hoặc hỏi đồng nghiệp; dashboard hiện chỉ đếm login và số câu hỏi |
| **Ngoài phạm vi** | Công cụ AI khác; phòng ban khác; để AI tự quyết định thay người trong ca |

**Tiêu chí hoàn thành từng quy trình** *(biết khi nào một lượt được tính là xong)*:

| Quy trình | Tài liệu trong phạm vi | Hoàn thành khi |
| --- | --- | --- |
| **Q1 Tra cứu** | SOP, chính sách, biểu mẫu, đầu mối trong danh mục nguồn ưu tiên | Câu trả lời có nguồn mở được và còn hiệu lực; người dùng áp dụng được vào ca mà không phải tìm lại hay hỏi người |
| **Q2 Tóm tắt** | SOP, chính sách và thông báo thay đổi quy định trong danh mục nguồn ưu tiên; tài liệu ngoài danh mục không tóm tắt | Bản tóm tắt có đủ các mục bắt buộc (điều kiện áp dụng, ngoại lệ, hạn/hiệu lực, người phê duyệt), không thêm nội dung không có trong nguồn, kèm nguồn và ngày cập nhật |
| **Q3 Kiểm chứng và báo lỗi** | Mọi câu trả lời từ Q1 và Q2 | Việc có tác động đã được mở nguồn kiểm tra; nếu sai thì lỗi được ghi, gửi đúng data owner, xử lý trong hạn và người báo được biết kết quả |

*Danh mục nguồn ưu tiên là danh sách tài liệu thuộc phạm vi pilot, lập ở ngày 0–30 (Gate 1).*

**Một câu phạm vi:** *Với nhân viên vận hành, làm cho trợ lý tra cứu trở thành một bước đáng tin cậy trong ba quy trình tra cứu → tóm tắt → kiểm chứng, thay vì tìm file thủ công.*

---

## 2. Hiện trạng: deployment hay adoption?

Đã **deployment** (công cụ được cấp phát) nhưng chưa **adoption** (workflow, owner và bàn giao chưa đổi). Kiểm bằng năm yếu tố:

| # | Yếu tố | Hiện trạng (theo ví dụ của đề) | Đích ngày 90 |
| --- | --- | --- | --- |
| 1 | Công việc | Trợ lý nằm ngoài bước tra cứu chính thức | Bước "hỏi AI → xem nguồn → kiểm tra → dùng/báo lỗi" ghi trong SOP của Q1–Q3 |
| 2 | Trách nhiệm | Không ai chịu trách nhiệm chất lượng câu trả lời | Mỗi tài liệu có data owner; trưởng ca chịu trách nhiệm kết quả cuối |
| 3 | Kiểm soát | Không trích nguồn, không kiểm tra mẫu, không cách báo lỗi | Có đủ chuỗi Nguồn → Trích nguồn → QA mẫu → Chuyển người → Phản hồi |
| 4 | Hành vi | Người dùng chưa biết khi nào nên tin | Có quy tắc "dùng / không dùng / chuyển người" và người dẫn dắt tại ca |
| 5 | Đo lường | Chỉ đo login và số câu hỏi | Có mốc đầu, mục tiêu, nguồn, owner, hành động cho mọi chỉ số quyết định |

---

## 3. Chẩn đoán

### 3.1 Năm câu hỏi

| Trục | Nhận định | Mức |
| --- | --- | --- |
| Workflow | AI nằm ngoài bước tra cứu chính thức; chưa có bàn giao | **Gốc** |
| Con người | Chưa biết khi nào tin được câu trả lời (thiếu tin tưởng, không phải thiếu động lực) | Liên quan |
| Sẵn sàng | Nguồn tài liệu thiếu người phụ trách và lịch cập nhật | Liên quan |
| Tin cậy | Không trích nguồn, không kiểm tra mẫu, không cách báo lỗi | **Gốc** |
| Đo lường | Chỉ đo lượt dùng; chưa đo thời gian, làm lại, chất lượng | Liên quan |

### 3.2 Gartner-Lite — sẵn sàng chưa? *(dùng cho readiness)*

| Hạng mục | Nhận định (theo ví dụ của đề) | Kết quả | Cách xác nhận khi triển khai thật |
| --- | --- | --- | --- |
| Hướng đi | Mục tiêu rõ: giảm thời gian tìm tài liệu nội bộ | Đạt | Sponsor xác nhận bằng văn bản |
| Dữ liệu | Nguồn thiếu người phụ trách và lịch cập nhật | Thiếu | Kiểm kê tài liệu trong phạm vi (cột owner, ngày cập nhật) |
| Governance | Quyền truy cập và phạm vi tài liệu chưa thống nhất | Thiếu | Đối chiếu danh sách quyền với danh sách tài liệu |
| Vận hành | Chưa có owner chất lượng câu trả lời | Thiếu | Hỏi trực tiếp: "ai nhận báo lỗi?" |
| Hấp thụ | Chưa có hỗ trợ và vòng phản hồi lỗi | Thiếu | Kiểm tra có kênh báo lỗi và người xử lý hay chưa |

**Kết luận:** pilot nhỏ để sửa readiness; **chưa rollout rộng.** *Gartner-Lite chỉ trả lời "sẵn sàng chưa, có nên rollout rộng không"; nó không chứng minh nguyên nhân gốc (xem 3.4).*

### 3.3 ADKAR — người dùng kẹt ở đâu? *(dùng cho người dùng)*

| Bước | Nhận định | Trạng thái | Giải pháp đặt ngay tại workflow |
| --- | --- | --- | --- |
| Awareness | Chưa rõ nên dùng AI cho loại câu hỏi nào | **Nghẽn** | Danh sách "nên hỏi / không nên hỏi / chuyển người" gắn ở màn hình tra cứu |
| Desire | Ngại tin vì không thấy nguồn | **Nghẽn** | Mọi câu trả lời hiện nguồn + ngày cập nhật, mở được một cú bấm |
| Knowledge | Chưa biết cách hỏi và kiểm chứng nguồn | Cần làm | Thẻ hướng dẫn 1 trang theo đúng quy trình Q1–Q3 |
| Ability | Chưa thực hành trong tra cứu thật | Cần làm | Làm thử trên ca thật cùng người dẫn dắt (không dạy riêng ngoài ca) |
| Reinforcement | Chưa có phản hồi lỗi và theo dõi hành vi | Cần làm | Báo cáo tuần: lỗi đã sửa, ai báo; trưởng ca nhắc bước chuẩn |

**Kết luận:** đào tạo là chưa đủ, vì nghẽn nằm ở Desire; cần **nguồn kiểm chứng, hướng dẫn và hỗ trợ ngay tại workflow.**

### 3.4 Hai nguyên nhân gốc

Triệu chứng là "ít người quay lại dùng". Hỏi tiếp *ít dùng vì sao?* thì xuống tới hai nguyên nhân:

| | Nguyên nhân gốc | Framework | Bằng chứng |
| --- | --- | --- | --- |
| **RC1** | **Độ tin cậy:** câu trả lời không có nguồn và ngày cập nhật; không có QA mẫu, không có cách báo lỗi, nên người dùng không có cơ sở để tin | 5 câu hỏi (Tin cậy) · ADKAR (Desire) · Gartner-Lite (chỉ đánh giá readiness: dữ liệu) | **Case:** Morgan Stanley (xem 3.5). **Hiện trường (kế hoạch):** phép thử 20 câu hỏi (3.5) |
| **RC2** | **Workflow và chia việc:** trợ lý không nằm trong bước tra cứu chính thức; chưa nói rõ ai kiểm chứng, ai chịu trách nhiệm, chuyển người ở đâu khi AI không chắc | 5 câu hỏi (Workflow) · Mollick (chia việc) · Gartner-Lite (chỉ đánh giá readiness: owner) | **Case:** Klarna (xem 3.5). **Hiện trường (kế hoạch):** quan sát hành vi (phiếu phần B, 3.5) |

**Phân vai bằng chứng:** 5 câu hỏi, ADKAR và Mollick giúp *định vị* nguyên nhân; Gartner-Lite chỉ đánh giá readiness. Hai nguyên nhân gốc hiện là **giả thuyết có case tham khảo ủng hộ**, chỉ được coi là xác nhận khi phép thử 20 câu và quan sát hành vi (3.5) cho kết quả khớp bảng "cách đọc nhanh" trong [phiếu](phieu-bang-chung.md).

*Đo lường* và *Con người* được ghi là nguyên nhân liên quan, không phải gốc: đo sai khiến không thấy vấn đề, nhưng không gây ra vấn đề.

### 3.5 Bằng chứng

**Case tham khảo thật** *(lấy bài học thiết kế, không lấy con số)*:

- **Morgan Stanley → RC1.** Trợ lý nội bộ cho cố vấn tài chính được mở rộng sau khi có khung đánh giá: kiểm tra hằng ngày bằng bộ câu hỏi mẫu, chuyên gia con người tham gia chấm, chỉnh truy xuất liên tục. Công ty báo trên 98% nhóm cố vấn dùng, nhưng đó là số tự công bố và "có dùng" chưa bằng "dùng hiệu quả". *Bài học: độ tin cậy đi trước mở rộng.*
- **Klarna → RC2.** Công ty từng công bố trợ lý AI làm việc của khoảng 700 nhân viên; năm 2025 CEO nói chi phí đã được đặt nặng quá mức, dẫn tới chất lượng thấp hơn, và tuyển lại nhân viên để khách luôn tìm được người thật. *Bài học: khối lượng tự động hoá không thay thế chất lượng và đường chuyển sang người.*
- **DWP / GDS → thiết kế chỉ số (mục 6).** Đánh giá của DWP có nhóm so sánh (người dùng vs không dùng) ra mức tiết kiệm khiêm tốn hơn con số tự khai của nghiên cứu GDS không có nhóm so sánh. *Bài học: nhóm đối chứng đáng tin hơn tự khai.*

**Kế hoạch bằng chứng hiện trường** *(chưa thực hiện vì bài tập không có công cụ AI thật để đo; làm ở tuần 1 của pilot thật; mỗi mục có điều kiện bác bỏ để khỏi chọn bằng chứng theo ý mình)*:

| Phép thử | Cách làm | Nếu kết quả là... thì... |
| --- | --- | --- |
| **Thử 20 câu hỏi** (RC1) | Phiếu phần A: chạy 20 câu hỏi (bộ mẫu, thay bằng câu thật khi triển khai) qua trợ lý, chấm: có nguồn? có ngày? đúng và còn hiệu lực? | P1 và P2 đều ≥ 90% mà người dùng vẫn ít dùng → RC1 yếu, chuyển sang Awareness/Desire |
| **Tự quan sát hành vi** (RC2, ADKAR) | Phiếu phần B: người dùng ghi mở trợ lý ở bước nào, sau khi nhận câu trả lời làm gì, lý do lần gần nhất không dùng | Chủ yếu **mở trợ lý ngay từ đầu trong quy trình** → RC2 yếu |
| *Phỏng vấn 3–5 người* (tuỳ chọn) | 3 câu: *Lần gần nhất bạn không dùng trợ lý là khi nào, vì sao? · Bạn biết nó đúng bằng cách nào? · Sai thì báo ai?* | Lý do chính là "không biết dùng" → quay lại Knowledge/Ability |

Phiếu ghi sẵn: [phieu-bang-chung.md](phieu-bang-chung.md) (kế hoạch, kèm cách đọc kết quả). **Với bài tập này, căn cứ chẩn đoán là ba case tham khảo ở trên** (đủ yêu cầu "≥1 căn cứ"). Kết quả đo thật khi triển khai: chưa có.

---

## 4. Thiết kế cách làm mới

### 4.1 AS-IS / TO-BE

| AS-IS (hiện tại) | TO-BE (sau thiết kế) |
| --- | --- |
| Tìm file trong nhiều thư mục | **Hỏi trợ lý** theo quy trình (Q1) |
| Hỏi đồng nghiệp, phụ thuộc kinh nghiệm | **Xem nguồn và ngày cập nhật** hiện cùng câu trả lời |
| Dùng tài liệu mà khó biết bản mới nhất | **Kiểm tra:** việc có tác động mở nguồn trước khi dùng; trưởng ca chịu trách nhiệm kết quả cuối |
| Không có đường báo sai | **Dùng hoặc báo lỗi** bằng một nút; data owner nhận và xử lý theo hạn |

### 4.2 Ba thay đổi bắt buộc

1. **Nguồn kiểm chứng:** mọi câu trả lời kèm nguồn + ngày cập nhật; không có nguồn hợp lệ thì không trả lời như thể chắc chắn.
2. **Người chịu trách nhiệm:** data owner cho từng tài liệu; trưởng ca cho kết quả cuối; Phụ trách AI cho chất lượng trợ lý.
3. **Cách xử lý khi AI không chắc:** trợ lý nói rõ "chưa chắc" và **chuyển người** (data owner hoặc trưởng ca) khi không có nguồn, nguồn quá hạn hoặc câu hỏi nằm ngoài phạm vi.

### 4.3 Chia việc người–AI *(Mollick)*

| Vùng | Việc cụ thể trong Q1–Q3 | Quy tắc |
| --- | --- | --- |
| **Người giữ quyền** | Quyết định áp dụng quy định vào ca; xử lý ngoại lệ; đánh giá rủi ro; duyệt và cập nhật nguồn; chịu trách nhiệm kết quả cuối | AI không quyết thay |
| **AI hỗ trợ, người kiểm** | Tìm tài liệu (Q1); tóm tắt và chỉ ra phần thay đổi (Q2); gợi ý nguồn liên quan | Người mở nguồn kiểm chứng trước khi dùng cho việc có tác động |
| **AI tự động, có kiểm soát** | Gắn nguồn và ngày cập nhật; cảnh báo tài liệu quá hạn; tự định tuyến báo lỗi tới data owner; trả lời câu hỏi rủi ro thấp (biểu mẫu, lịch, đầu mối) khi có nguồn còn hiệu lực | Chỉ tác vụ lặp lại, rủi ro thấp, có tiêu chí kiểm tra |

**Nguyên tắc:** AI tăng tốc tìm và tổng hợp; con người kiểm chứng và chịu trách nhiệm.

### 4.4 Kiến trúc tin cậy

| Bước | Cơ chế cụ thể | Owner | Đạt khi |
| --- | --- | --- | --- |
| Nguồn | Kiểm kê tài liệu trong phạm vi; mỗi tài liệu có data owner và lịch cập nhật | Data owner | Không tài liệu nào thiếu owner |
| Trích nguồn | Câu trả lời hiện tên tài liệu, trang/mục, ngày cập nhật | Phụ trách AI | Nguồn mở được từ câu trả lời |
| QA mẫu | Bộ câu hỏi vàng chạy định kỳ + chấm mẫu hằng tuần bởi 2 người độc lập | Chủ quy trình (vai QA) | Có báo cáo tuần |
| Chuyển người | Quy tắc "chưa chắc → chuyển data owner / trưởng ca" | Chủ quy trình | Mọi ca chưa chắc đều có người nhận |
| Phản hồi | Nút báo lỗi, SLA xử lý, báo cáo tuần các lỗi đã sửa | Phụ trách AI | Lỗi được xử lý đúng hạn và người báo được biết kết quả |

Bốn điều kiện sẵn sàng đi kèm: nguồn có người phụ trách và lịch cập nhật · quyền truy cập đúng người đúng mục đích · phạm vi dùng AI được định nghĩa rõ (mục 1, 4.3) · chi phí, năng lực vận hành và cơ chế quản trị *(ngân sách và người vận hành: cần Sponsor xác nhận)*.

---

## 5. Lộ trình 30–60–90 ngày

Mỗi giai đoạn là một cổng quyết định. **Gate mở khi chất lượng, hành vi và giá trị đạt mục tiêu đã xác nhận, không phải khi hết ngày.**

| Giai đoạn | Owner | Việc chính | Dấu hiệu hoàn thành (điều kiện qua gate) |
| --- | --- | --- | --- |
| **Ngày 0–30: Nền tin cậy** | **Phụ trách AI** (cùng Data owner) | Khoá phạm vi; kiểm kê nguồn và gán data owner; bật trích nguồn + ngày; dựng bộ câu hỏi vàng; mở kênh báo lỗi; xin quyền dữ liệu nghiệp vụ; **đo mốc đầu bằng [phiếu đo mốc đầu](phieu-bang-chung.md)** (P1, P2, W1, W2) và thu mốc đầu B1 từ hệ thống nghiệp vụ | **Gate 1:** kiểm kê xong, mọi tài liệu trong phạm vi có owner và lịch cập nhật · mốc đầu P1, P2, W1, W2 và **B1** đã đo và ghi (không lấy được B1: Sponsor quyết định ngay, xem mục 8) · kênh báo lỗi hoạt động · ≥1 vòng chấm mẫu hoàn tất · Sponsor ký |
| **Ngày 31–60: Pilot trong workflow** | **Chủ quy trình** | Đưa bước chuẩn vào SOP của Q1–Q3; chạy pilot ở 1 ca, giữ 1 ca đối chứng nếu có; hướng dẫn tại ca (ADKAR); chấm mẫu hằng tuần; xử lý lỗi theo hạn | **Gate 2:** P1, P2 đạt mục tiêu · W2 giảm so với mốc đầu · W1 giảm so với mốc đầu (và so với ca đối chứng nếu có) · không còn lỗi sai nghiêm trọng chưa xử lý |
| **Ngày 61–90: Đo giá trị và quyết định** | **Sponsor** (kèm Chủ quy trình) | Duy trì pilot; thu thêm các chỉ số cần dữ liệu thật (6B), nhất là kết quả nghiệp vụ; đánh giá chi phí vận hành | **Quyết định:** tiếp tục mở rộng / sửa / dừng, theo quy tắc ở mục 8 |

**Bốn vai trò** *(gộp cho pilot nhỏ, chưa gán tên)*:

| Vai trò | Phụ trách |
| --- | --- |
| **Sponsor** | Quản lý vận hành: ký gate, nhận memo, cấp quyền truy cập log và ngân sách |
| **Phụ trách AI** | Chất lượng trợ lý, trích nguồn, kênh báo lỗi |
| **Data owner** | Nguồn tài liệu, lịch cập nhật, sửa tài liệu bị báo lỗi |
| **Chủ quy trình** | Trưởng ca vận hành: SOP Q1–Q3, hành vi của ca, **chấm mẫu (QA)** và kết quả nghiệp vụ |

> **Rủi ro cần ghi:** Chủ quy trình vừa vận hành vừa chấm mẫu nên dễ thiên vị. Khi triển khai thật, chấm mẫu cần 2 người độc lập, một người ngoài ca.

---

## 6. Dashboard chỉ số (v2)

Theo dõi từ dưới lên, **ra quyết định dựa trên tầng 4–5**. Chỉ số có hai mức: **Product** (cả sản phẩm) và **Workflow** (từng quy trình). Vì đây là bài minh hoạ chưa có số đo thật, bộ chỉ số chia hai phần: 6A đo được ngay từ tuần 1 của pilot, 6B chỉ đo được khi triển khai thật (**chưa đặt mục tiêu**, theo quy tắc "không đặt mục tiêu cho chỉ số không lấy được số").

### 6A. Đo được ngay từ tuần 1 của pilot (bằng phiếu đo mốc đầu)

| # | Chỉ số *(loại · tầng)* | Mốc đầu | Mục tiêu *(đề xuất)* | Nguồn dữ liệu | Phụ trách | Khi xấu → hành động |
| --- | --- | --- | --- | --- | --- | --- |
| **P1** | **Tỷ lệ câu trả lời có nguồn kiểm chứng được** (có nguồn, mở được, còn hiệu lực) · *Product · tầng 4* | Tuần 1: chấm 20 câu hỏi theo phiếu (phần C) | ≥ 90% tại Gate 2 | Phiếu chấm mẫu; về sau bộ câu hỏi vàng + chấm hằng tuần | Chủ quy trình (vai QA) | **< 80% hai tuần liền** → dừng mở thêm người dùng; Phụ trách AI lập 10 lỗi hàng đầu, sửa nguồn/truy xuất trong 5 ngày làm việc; tăng gấp đôi cỡ mẫu chấm |
| **P2** | **Tỷ lệ trả lời đúng và đúng phiên bản** · *Product · tầng 4* | Cùng 20 câu | ≥ 90% tại Gate 2 | Phiếu chấm mẫu | Chủ quy trình (vai QA) | **Có lỗi sai nghiêm trọng** (dẫn tới xử lý sai ca) → ẩn tài liệu đó khỏi trợ lý ngay; Data owner sửa trong 2 ngày làm việc; báo Sponsor |
| **W1** | **Thời gian hoàn thành một lượt tra cứu** (median, giây; cách mới gồm cả bước mở nguồn) · *Workflow Q1 · tầng 3* | Phiếu: bấm giờ cặp 10 câu, cách thủ công vs qua trợ lý | Giảm ≥ 30% so với cách thủ công (và so với ca đối chứng khi có) | Phiếu bấm giờ; về sau log tác vụ | Chủ quy trình | **Không giảm sau 4 tuần pilot, hoặc giảm nhưng W2 xấu** → xem lại cách làm: quan sát 5 lượt, tìm bước nghẽn (truy xuất chậm hay kiểm chứng rườm) |
| **W2** | **Tỷ lệ lượt phải quay lại tìm thủ công hoặc hỏi người sau khi hỏi trợ lý** · *Workflow Q1–Q2 · tầng 4* | Phiếu: cột "Phải tìm lại hoặc hỏi người", 20 câu | Giảm ≥ 15 điểm % so với mốc đầu | Phiếu; về sau log QA / ticket mở lại | Chủ quy trình | **Không giảm hoặc tăng** → siết kiểm soát: bắt buộc mở nguồn trước khi dùng cho việc có tác động; chấm 100% mẫu trong tuần đó; xem lại P1, P2 |

W2 đo thẳng vào vấn đề quan sát được ("vẫn quay lại tìm file thủ công"), nên nó là chỉ số thay cho "tỷ lệ làm lại" của bản v1 khi chưa có log QA.

### 6B. Chỉ đo được khi triển khai thật *(chưa có dữ liệu, chưa đặt mục tiêu)*

| # | Chỉ số *(loại · tầng)* | Cần dữ liệu gì | Phụ trách | Hành động dự kiến khi xấu |
| --- | --- | --- | --- | --- |
| **W3** | Tỷ lệ lượt đi đúng bước chuẩn: hỏi AI → mở nguồn → xác nhận hoặc báo lỗi · *Workflow · tầng 2* | Log quy trình ("đã mở nguồn", "đã xác nhận") | Chủ quy trình | Hỏi 3 người bỏ bước, sửa giao diện/quy trình, chạy lại ADKAR cho Desire và Ability |
| **P3** | Tỷ lệ báo lỗi được xử lý trong hạn (3 ngày làm việc) · *Product · rủi ro/bàn giao* | Log báo lỗi (cần kênh báo lỗi đã mở ở Gate 1) | Phụ trách AI | Leo thang Sponsor; thêm người xử lý hoặc thu hẹp phạm vi tài liệu |
| **B1** | **Kết quả nghiệp vụ:** tỷ lệ ca xử lý đúng quy định lần đầu *(hoặc số lỗi do dùng tài liệu sai/lỗi thời)* · *Business · tầng 5* | Hệ thống nghiệp vụ / audit, so với ca đối chứng; **mốc đầu thu ở ngày 0–30, mục tiêu đặt tại Gate 1** | Chủ quy trình | Thu hẹp phạm vi (bỏ quy trình rủi ro) rồi sửa; **dừng** nếu hai vòng sửa không đảo ngược |

> **Hệ quả bắt buộc:** B1 là chỉ số giá trị duy nhất. Khi chưa có B1, dashboard chỉ chứng minh được đến tầng 4, nên quyết định cao nhất có thể ra lúc này là **SỬA**, chưa thể là "tiếp tục mở rộng" (mục 8). Để ngày 90 không thiếu căn cứ, mốc đầu B1 phải có từ Gate 1 (mục 5).

**Chỉ số theo dõi nhưng không dùng để quyết định:**

| Chỉ số | Vì sao chỉ làm bối cảnh |
| --- | --- |
| Số tài khoản đăng nhập, số câu hỏi, tỷ lệ lượt tra cứu có dùng trợ lý | Đo hoạt động, không đo giá trị; tăng được mà chất lượng không đổi, và tăng khi P1, P2 thấp chỉ làm tăng câu trả lời không đáng tin |
| Thời gian tiết kiệm **tự khai** | Chỉ để đối chiếu với W1 đo bằng bấm giờ hoặc log |

**Thiết kế đo:**

- **Tuần 1 của pilot (một người đo):** đối chứng ngay trong cá nhân: cùng 10 câu làm hai cách, lẻ thủ công trước, chẵn trợ lý trước. Chấm P1, P2, W2 trên 20 câu.
- **Khi triển khai thật:** một ca hoặc nhóm tương đương không dùng quy trình mới làm nhóm đối chứng; so pilot với đối chứng, không so với niềm tin.
- **Ước tính thận trọng:** dùng median, bỏ ngoại lệ, báo khoảng chứ không báo một con số đẹp.
- **Mốc đầu:** ghi rõ ai đo, mẫu bao nhiêu, đo bằng nguồn nào. Mốc đầu tuần 1 dự kiến là **một người đo, một người chấm, mẫu nhỏ**: dùng để đặt mục tiêu, không dùng để kết luận cho cả tổ chức.

**Mapping năm tầng:** đo được ngay: tầng 3 (W1), tầng 4 (P1, P2, W2). Cần dữ liệu thật: tầng 2 (W3), tầng 4–bàn giao (P3), tầng 5 (B1). Tầng 1 chỉ là bối cảnh.

---

## 7. Kiểm tra chéo: v1 → v2

### 7.1 Dashboard v1 (dựng lại từ mẫu 4.5)

Bản v1 dưới đây được dựng lại bằng cách điền nguyên mẫu 4.5 cho tình huống này; không phải bản đã nộp ở checkpoint phút 80. Nếu bạn có bản v1 thật, thay vào đây.

| Chỉ số | Mốc đầu | Mục tiêu | Nguồn dữ liệu | Phụ trách | Khi chỉ số xấu |
| --- | --- | --- | --- | --- | --- |
| Mức dùng theo quy trình | Đo tuần 1 | Mục tiêu nhóm | Log quy trình | Trưởng nhóm | Tìm điểm vướng |
| Thời gian xử lý | Đo hiện trạng | Mục tiêu nhóm | Log tác vụ | Chủ quy trình | Xem lại cách làm |
| Tỷ lệ có nguồn | Đo mẫu | Mục tiêu nhóm | Kiểm tra mẫu | Phụ trách QA | Tăng kiểm soát |
| Kết quả nghiệp vụ | Số hiện tại | Mục tiêu nhóm | Hệ thống nghiệp vụ | Chủ nghiệp vụ | Điều chỉnh / dừng |
| Rủi ro / bàn giao | Ghi hiện trạng | Ngưỡng nhóm | Log lỗi | Phụ trách AI | Bổ sung xử lý |

Lộ trình v1: 30 ngày triển khai trích nguồn · 60 ngày pilot · 90 ngày đánh giá, chuyển giai đoạn theo mốc ngày. TO-BE v1: chèn thêm bước "hỏi AI" vào quy trình cũ.

### 7.2 Góp ý và thay đổi

> **Nguồn các góp ý dưới đây:** phản biện theo bốn trục của mục 4.6 và bảng lỗi thường gặp (5.3) áp lên v1. **Đây chưa phải góp ý của người khác.** Góp ý thật nhận được ghi ở 7.3 bên dưới.

| # | Trục | Góp ý cụ thể về v1 | Thay đổi trong v2 |
| --- | --- | --- | --- |
| 1 | Chỉ số | Cột "Mục tiêu" chỉ ghi "mục tiêu nhóm" và cột "Khi xấu" chỉ là cụm chung ("Tìm điểm vướng", "Tăng kiểm soát"): không nói được **xấu là bao nhiêu và làm gì, trong bao lâu** | Mỗi chỉ số có mục tiêu (đề xuất), ngưỡng kích hoạt, hành động cụ thể, người làm và thời hạn (mục 6) |
| 2 | Chỉ số | "Mức dùng theo quy trình" đứng đầu bảng và là điều kiện chuyển giai đoạn: thưởng cho việc dùng nhiều dù trả lời chưa đáng tin | Hạ xuống thành chỉ số bối cảnh; gate dựa trên tầng 3–4, và tầng 5 khi triển khai thật (mục 5, 6) |
| 3 | Chỉ số | Thời gian xử lý không có nhóm so sánh; "đo hiện trạng" không nói ai đo, mẫu bao nhiêu | Thêm đối chứng (cùng câu hỏi làm hai cách khi đo một mình; ca đối chứng khi triển khai thật), dùng median, ghi mẫu và người đo; tự khai chỉ để đối chiếu (mục 6) |
| 4 | Hành động | Lộ trình chuyển theo ngày, thiếu dấu hiệu hoàn thành và owner mỗi giai đoạn: thành danh sách việc | Mỗi giai đoạn có owner; hai gate theo bằng chứng; giai đoạn 3 kết thúc bằng quyết định (mục 5) |
| 5 | Framework | TO-BE chỉ chèn bước "hỏi AI", chưa nói ai kiểm chứng, ai chịu trách nhiệm, AI không chắc thì sao | Thêm chia việc Mollick, ba thay đổi bắt buộc và chuỗi tin cậy có owner (mục 4) |

### 7.3 Góp ý thật từ người phản biện

| Người phản biện | Trục | Góp ý | Có nhận không? | Thay đổi |
| --- | --- | --- | --- | --- |
| ⏳ *(điền tên; nếu là công cụ AI thì ghi rõ tên công cụ)* | Phạm vi | "Tóm tắt" chưa nói rõ tài liệu nào và tiêu chí thế nào thì được xem là hoàn thành | Nhận | Mục 1: Q2 giới hạn trong danh mục nguồn ưu tiên; thêm bảng tiêu chí hoàn thành cho Q1–Q3 |
| (như trên) | Framework | Gartner-Lite chỉ cho biết thiếu/đạt readiness, chưa tự chứng minh nguyên nhân gốc; bằng chứng gốc phải đến từ phép thử 20 câu và quan sát hành vi | Nhận | Mục 3.2 và 3.4: ghi rõ Gartner-Lite chỉ đánh giá readiness; hai nguyên nhân gốc là giả thuyết, chờ phép thử xác nhận |
| (như trên) | Chỉ số, Hành động | B1 chưa có dữ liệu nên chưa chứng minh được giá trị; ở ngày 90 vẫn có thể thiếu căn cứ để chọn "tiếp tục" | Nhận một phần (bài tập không có dữ liệu thật để đo B1) | Mục 5, 6B, 8: mốc đầu B1 và quyền dữ liệu phải có từ Gate 1; thiếu thì Sponsor quyết định ngay ở ngày 30 |
| (như trên) | Quyết định | Chọn SỬA: chỉ mở rộng khi chất lượng, hiệu quả quy trình và kết quả nghiệp vụ cùng đạt ngưỡng | Đồng ý | Không đổi |

---

## 8. Quyết định

**Quyết định hiện tại (14/10/2026): SỬA.** Tiếp tục với pilot nhỏ để sửa độ tin cậy và quy trình **trước**; chưa mở rộng và chưa dùng lượt dùng làm thước đo thành công.

**Mốc kiểm tra sớm:** nếu đến Gate 1 (ngày 30) chưa có quyền truy cập dữ liệu nghiệp vụ hoặc mốc đầu B1, Sponsor quyết định ngay: cấp quyền, hoặc chấp nhận trần quyết định là SỬA. Không để đến ngày 90 mới phát hiện thiếu căn cứ để chọn "tiếp tục".

**Quy tắc quyết định tại ngày 90:**

| Quyết định | Khi nào |
| --- | --- |
| **Tiếp tục / mở rộng** | P1, P2 đạt mục tiêu · W2 và W1 đạt mục tiêu · **B1 đã đo** và cải thiện so với ca đối chứng, giữ được 4 tuần · không có lỗi sai nghiêm trọng đang tồn tại. *Chưa có B1 thì không ra quyết định này.* |
| **Sửa** | Tầng 3 đạt nhưng tầng 4 chưa đạt; hoặc đã xác định được nguyên nhân và còn một vòng sửa; hoặc chưa đo được B1 |
| **Dừng** | Sau hai vòng sửa, tầng 4 vẫn không đạt; hoặc B1 xấu hơn đối chứng; hoặc chi phí vận hành lớn hơn giá trị đo được |

---

## 9. Năm câu tự kiểm

- [x] 1. **AI đi vào quy trình nào?** Q1 tra cứu · Q2 tóm tắt · Q3 kiểm chứng và báo lỗi (mục 1)
- [x] 2. **Nguyên nhân gốc nằm ở đâu?** RC1 độ tin cậy · RC2 workflow và chia việc (3.4)
- [x] 3. **Framework nào giúp trả lời?** Gartner-Lite cho readiness (3.2) · ADKAR cho người dùng (3.3) · Mollick cho chia việc (4.3)
- [x] 4. **Chỉ số nào chứng minh giá trị?** P1, P2 (tin cậy) · W1, W2 (quy trình) đo được ngay ở tuần 1 bằng phiếu; B1 (nghiệp vụ) khi triển khai thật (mục 6)
- [x] 5. **Khi nào tiếp tục, sửa hoặc dừng?** Hiện tại *sửa*; quy tắc ở mục 8

---

## 10. Việc còn lại trước khi nộp ⏳

1. **Điền tên người phản biện** vào dòng đầu bảng 7.3. Nếu phản biện do một công cụ AI thực hiện thì ghi rõ tên công cụ; nếu do bạn học thì ghi họ tên.
2. **Mở các link nguồn tham khảo** cuối file để kiểm tra lại chi tiết các case.
3. *Tuỳ chọn, chỉ khi có công cụ AI thật:* làm [phiếu đo mốc đầu](phieu-bang-chung.md) và điền kết quả vào 3.5 và 6A.

---

## Nguồn tham khảo

- OpenAI — [Morgan Stanley](https://openai.com/index/morgan-stanley/): trợ lý nội bộ cho cố vấn, khung đánh giá, mức dùng do công ty công bố.
- GOV.UK — [An Evaluation of DWP's Microsoft 365 Copilot Trial](https://www.gov.uk/government/publications/an-evaluation-of-dwps-microsoft-copilot-365-trial/an-evaluation-of-dwps-microsoft-365-copilot-trial) và [The Register](https://www.theregister.com/2026/02/04/dwp_finds_copilot_saves_civil/): so sánh nhóm dùng với nhóm không dùng, đối chiếu với nghiên cứu GDS tự khai.
- Computing — [Klarna rows back on AI](https://www.computing.co.uk/news/2025/ai/meat-back-on-the-menu-as-klarna-rows-back-on-ai) và [Entrepreneur](https://www.entrepreneur.com/business-news/klarna-ceo-reverses-course-by-hiring-more-humans-not-ai/491396): tuyển lại nhân viên sau khi chất lượng giảm.
- Khung: Prosci ADKAR · Gartner AI Maturity Model (bản rút gọn Gartner-Lite trong đề) · Mollick, *Centaurs and Cyborgs* · NIST AI RMF.
