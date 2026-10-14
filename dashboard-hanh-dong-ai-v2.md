# Dashboard hành động cho áp dụng AI — v2

**Sản phẩm:** Trợ lý AI tra cứu tài liệu nội bộ · **Nhóm:** ⏳ *(điền tên nhóm)* · **Ngày:** 14/10/2026

> **Cách đọc file này**
> - Tình huống nền là *ví dụ xuyên suốt của đề* (minh hoạ, không phải số liệu của một doanh nghiệp cụ thể). Nhóm phải đối chiếu với tình huống thật của mình ở mọi ô có dấu ⏳.
> - **Không có số đo thực nào trong file.** Mọi "mốc đầu" là *cách đo + thời điểm đo*, không phải con số. Mọi mục tiêu ghi **(đề xuất)** là giá trị khởi điểm, nhóm xác nhận sau khi có mốc đầu.
> - ⏳ = nhóm điền hoặc xác nhận bằng dữ liệu thật trước khi nộp. Danh sách việc còn lại ở mục 10.

---

## 1. Phạm vi đã khoá

| | |
| --- | --- |
| **Sản phẩm AI** | Trợ lý AI tra cứu tài liệu nội bộ (một sản phẩm duy nhất) |
| **Người dùng chính** | Nhân viên vận hành |
| **Quy trình (3)** | **Q1 Tra cứu** quy trình/chính sách khi xử lý một ca · **Q2 Tóm tắt** tài liệu dài hoặc thay đổi quy định cho ca làm việc · **Q3 Kiểm chứng và báo lỗi** nguồn trước khi dùng |
| **Vấn đề quan sát được** | Nhân viên vẫn quay lại tìm file thủ công hoặc hỏi đồng nghiệp; dashboard hiện chỉ đếm login và số câu hỏi |
| **Ngoài phạm vi** | Công cụ AI khác; phòng ban khác; để AI tự quyết định thay người trong ca |

**Một câu phạm vi:** *Với nhân viên vận hành, làm cho trợ lý tra cứu trở thành một bước đáng tin cậy trong ba quy trình tra cứu → tóm tắt → kiểm chứng, thay vì tìm file thủ công.*

---

## 2. Hiện trạng: deployment hay adoption?

Đã **deployment** (công cụ được cấp phát) nhưng chưa **adoption** (workflow, owner và bàn giao chưa đổi). Kiểm bằng năm yếu tố:

| # | Yếu tố | Hiện trạng ⏳ (xác nhận) | Đích ngày 90 |
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

| Hạng mục | Nhận định ⏳ | Kết quả | Xác nhận bằng |
| --- | --- | --- | --- |
| Hướng đi | Mục tiêu rõ: giảm thời gian tìm tài liệu nội bộ | Đạt | Sponsor xác nhận bằng văn bản |
| Dữ liệu | Nguồn thiếu người phụ trách và lịch cập nhật | Thiếu | Kiểm kê tài liệu trong phạm vi (cột owner, ngày cập nhật) |
| Governance | Quyền truy cập và phạm vi tài liệu chưa thống nhất | Thiếu | Đối chiếu danh sách quyền với danh sách tài liệu |
| Vận hành | Chưa có owner chất lượng câu trả lời | Thiếu | Hỏi trực tiếp: "ai nhận báo lỗi?" |
| Hấp thụ | Chưa có hỗ trợ và vòng phản hồi lỗi | Thiếu | Kiểm tra có kênh báo lỗi và người xử lý hay chưa |

**Kết luận:** pilot nhỏ để sửa readiness; **chưa rollout rộng.**

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
| **RC1** | **Độ tin cậy:** câu trả lời không có nguồn và ngày cập nhật; không có QA mẫu, không có cách báo lỗi, nên người dùng không có cơ sở để tin | 5 câu hỏi (Tin cậy) · ADKAR (Desire) · Gartner-Lite (Readiness: dữ liệu) | **Case:** Morgan Stanley (xem 3.5). **Hiện trường ⏳:** phép thử 20 câu hỏi thật (3.5) |
| **RC2** | **Workflow và chia việc:** trợ lý không nằm trong bước tra cứu chính thức; chưa nói rõ ai kiểm chứng, ai chịu trách nhiệm, chuyển người ở đâu khi AI không chắc | 5 câu hỏi (Workflow) · Mollick (chia việc) · Gartner-Lite (Absorption: owner) | **Case:** Klarna (xem 3.5). **Hiện trường ⏳:** quan sát 10 lượt tra cứu (3.5) |

*Đo lường* và *Con người* được ghi là nguyên nhân liên quan, không phải gốc: đo sai khiến không thấy vấn đề, nhưng không gây ra vấn đề.

### 3.5 Bằng chứng

**Case tham khảo thật** *(lấy bài học thiết kế, không lấy con số)*:

- **Morgan Stanley → RC1.** Trợ lý nội bộ cho cố vấn tài chính được mở rộng sau khi có khung đánh giá: kiểm tra hằng ngày bằng bộ câu hỏi mẫu, chuyên gia con người tham gia chấm, chỉnh truy xuất liên tục. Công ty báo trên 98% nhóm cố vấn dùng, nhưng đó là số tự công bố và "có dùng" chưa bằng "dùng hiệu quả". *Bài học: độ tin cậy đi trước mở rộng.*
- **Klarna → RC2.** Công ty từng công bố trợ lý AI làm việc của khoảng 700 nhân viên; năm 2025 CEO nói chi phí đã được đặt nặng quá mức, dẫn tới chất lượng thấp hơn, và tuyển lại nhân viên để khách luôn tìm được người thật. *Bài học: khối lượng tự động hoá không thay thế chất lượng và đường chuyển sang người.*
- **DWP / GDS → thiết kế chỉ số (mục 6).** Đánh giá của DWP có nhóm so sánh (người dùng vs không dùng) ra mức tiết kiệm khiêm tốn hơn con số tự khai của nghiên cứu GDS không có nhóm so sánh. *Bài học: nhóm đối chứng đáng tin hơn tự khai.*

**Bằng chứng hiện trường ⏳** *(nhóm thu thập trước checkpoint phút 40; mỗi mục có điều kiện bác bỏ để khỏi chọn bằng chứng theo ý mình)*:

| Phép thử | Cách làm | Nếu kết quả là... thì... |
| --- | --- | --- |
| **Thử 20 câu hỏi thật** (RC1) | Lấy 20 câu nhân viên hay hỏi, chạy qua trợ lý, chấm: có nguồn? có ngày? đúng và còn hiệu lực? | Phần lớn **đã có nguồn và đúng** mà vẫn ít dùng → RC1 sai, chuyển sang Awareness/Desire |
| **Quan sát 10 lượt tra cứu** (RC2) | Ngồi cạnh 10 lượt tra cứu thật: người dùng mở trợ lý ở bước nào, hay bỏ qua? Lỗi thì làm gì? | Hầu hết lượt **có mở trợ lý trong quy trình** → RC2 sai |
| **Phỏng vấn 3–5 người** (RC1, ADKAR) | 3 câu: *Lần gần nhất bạn không dùng trợ lý là khi nào, vì sao? · Bạn biết nó đúng bằng cách nào? · Sai thì báo ai?* | Lý do chính là "không biết dùng" → quay lại Knowledge/Ability |

Ghi kết quả vào đây: ⏳ *(ngày, số mẫu, kết quả, người ghi)*

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
| QA mẫu | Bộ câu hỏi vàng chạy định kỳ + chấm mẫu hằng tuần bởi 2 người độc lập | Phụ trách QA | Có báo cáo tuần |
| Chuyển người | Quy tắc "chưa chắc → chuyển data owner / trưởng ca" | Chủ quy trình | Mọi ca chưa chắc đều có người nhận |
| Phản hồi | Nút báo lỗi, SLA xử lý, báo cáo tuần các lỗi đã sửa | Phụ trách AI | Lỗi được xử lý đúng hạn và người báo được biết kết quả |

Bốn điều kiện sẵn sàng đi kèm: nguồn có người phụ trách và lịch cập nhật · quyền truy cập đúng người đúng mục đích · phạm vi dùng AI được định nghĩa rõ (mục 1, 4.3) · chi phí, năng lực vận hành và cơ chế quản trị ⏳ *(điền ngân sách và người vận hành)*.

---

## 5. Lộ trình 30–60–90 ngày

Mỗi giai đoạn là một cổng quyết định. **Gate mở khi chất lượng, hành vi và giá trị đạt mục tiêu đã xác nhận, không phải khi hết ngày.**

| Giai đoạn | Owner | Việc chính | Dấu hiệu hoàn thành (điều kiện qua gate) |
| --- | --- | --- | --- |
| **Ngày 0–30: Nền tin cậy** | **Phụ trách AI** (chung với Data owner) | Khoá phạm vi; kiểm kê nguồn và gán data owner; bật trích nguồn + ngày; dựng bộ câu hỏi vàng; mở kênh báo lỗi; **đo mốc đầu tuần 1** | **Gate 1:** P4 = 100% tài liệu có owner và lịch cập nhật · có mốc đầu đủ cho P1, P2, W1, W2, B1 · kênh báo lỗi hoạt động · ≥1 vòng QA mẫu hoàn tất · Sponsor ký |
| **Ngày 31–60: Pilot trong workflow** | **Chủ quy trình** (trưởng ca vận hành) | Đưa bước chuẩn vào SOP của Q1–Q3; chạy pilot ở 1 ca/nhóm, giữ 1 nhóm đối chứng; hướng dẫn tại ca (ADKAR); QA mẫu hằng tuần; xử lý lỗi theo SLA | **Gate 2:** P1, P2 đạt mục tiêu · W3 đạt mục tiêu · W1 giảm so với mốc đầu **và** so với nhóm đối chứng · W2 và B1 không xấu đi |
| **Ngày 61–90: Đo giá trị và quyết định** | **Sponsor** (quản lý vận hành) cùng **Chủ nghiệp vụ** | Duy trì pilot, so sánh với nhóm đối chứng, đánh giá kết quả nghiệp vụ và chi phí vận hành | **Quyết định:** tiếp tục mở rộng / sửa / dừng, theo quy tắc ở mục 8 |

**Người đảm nhận từng vai trò:** Sponsor ⏳ · Phụ trách AI ⏳ · Data owner ⏳ · Chủ quy trình ⏳ · Phụ trách QA ⏳ · Chủ nghiệp vụ ⏳ · Trưởng nhóm ⏳

---

## 6. Dashboard chỉ số (v2)

Theo dõi từ dưới lên, **ra quyết định dựa trên tầng 4–5**. Chỉ số có hai mức: **Product** (cả sản phẩm) và **Workflow** (từng quy trình).

| # | Chỉ số *(loại · tầng)* | Mốc đầu | Mục tiêu *(đề xuất)* | Nguồn dữ liệu | Phụ trách | Khi xấu → hành động |
| --- | --- | --- | --- | --- | --- | --- |
| **P1** | **Tỷ lệ câu trả lời có nguồn kiểm chứng được** (có nguồn, mở được, còn hiệu lực) · *Product · tầng 4* | Tuần 1: chấm 30 câu hỏi vàng + 30 câu ngẫu nhiên từ log | ≥ 90% tại Gate 2 | Bộ câu hỏi vàng + chấm mẫu hằng tuần (2 người chấm độc lập) | Phụ trách QA | **< 80% hai tuần liền** → dừng mở thêm người dùng; Phụ trách AI lập 10 lỗi hàng đầu và sửa nguồn/truy xuất trong 5 ngày làm việc; tăng gấp đôi cỡ mẫu chấm |
| **P2** | **Tỷ lệ trả lời đúng và đúng phiên bản** theo chấm mẫu · *Product · tầng 4* | Cùng mẫu tuần 1 | ≥ 90% tại Gate 2 | Chấm mẫu hằng tuần | Phụ trách QA | **Có lỗi sai nghiêm trọng** (dẫn tới xử lý sai ca) → ẩn tài liệu đó khỏi trợ lý ngay, data owner sửa trong 2 ngày làm việc, báo trưởng ca |
| **P3** | **Tỷ lệ báo lỗi được xử lý trong SLA** (3 ngày làm việc) · *Product · rủi ro/bàn giao* | Chưa có kênh → đo từ tuần 2 | ≥ 90% | Log báo lỗi | Phụ trách AI | **< 70%** → leo thang Sponsor; bổ sung người xử lý hoặc thu hẹp phạm vi tài liệu |
| **P4** | **Tỷ lệ tài liệu có owner và lịch cập nhật còn hạn** · *Product · readiness* | Tuần 1: kiểm kê toàn bộ tài liệu trong phạm vi | 100% tại Gate 1 | Bảng kiểm kê nguồn | Data owner | **Tài liệu không có owner** → loại khỏi nguồn truy xuất cho tới khi có owner |
| **W1** | **Thời gian hoàn thành một lượt tra cứu** (median, phút) · *Workflow Q1 · tầng 3* | Tuần 1: log tác vụ + bấm giờ 20 lượt thật | Giảm so với mốc đầu và so với nhóm đối chứng; mức giảm ≥ 30% | Log tác vụ (thời điểm mở và đóng lượt tra cứu) | Chủ quy trình | **Không giảm sau 4 tuần pilot, hoặc giảm nhưng W2 xấu** → xem lại cách làm: quan sát 5 lượt, tìm bước nghẽn (truy xuất chậm hay kiểm chứng rườm) |
| **W2** | **Tỷ lệ lượt hoàn thành không phải làm lại** (không bị QA/trưởng ca trả về, không phải hỏi lại đồng nghiệp) · *Workflow Q1+Q2 · tầng 4* | Tuần 1: mẫu hồ sơ ca | Tăng 15 điểm % so với mốc đầu | Log QA rework / ticket mở lại | Phụ trách QA | **Làm lại tăng** → siết kiểm soát: bắt buộc mở nguồn trước khi dùng cho việc có tác động; QA 100% mẫu trong tuần đó |
| **W3** | **Tỷ lệ lượt đi đúng bước chuẩn** (hỏi AI → mở nguồn → xác nhận hoặc báo lỗi) · *Workflow Q1–Q3 · tầng 2* | Bước chưa tồn tại; ghi từ khi pilot bắt đầu | ≥ 70% tại Gate 2 | Log quy trình (trường "đã mở nguồn", "đã xác nhận") | Trưởng nhóm | **< 50% sau 2 tuần** → tìm điểm vướng: hỏi 3 người bỏ bước, sửa giao diện/quy trình; chạy lại ADKAR cho Desire và Ability |
| **B1** | **Kết quả nghiệp vụ:** tỷ lệ ca xử lý đúng quy định lần đầu *(hoặc số lỗi do dùng tài liệu sai/lỗi thời)* · *Business · tầng 5* | Tuần 1–2: lấy từ hệ thống nghiệp vụ/audit | Cải thiện so với nhóm đối chứng; **không được xấu đi** | Hệ thống nghiệp vụ / audit | Chủ nghiệp vụ | **Nhóm pilot xấu hơn đối chứng** → thu hẹp phạm vi (bỏ quy trình rủi ro), sửa; **dừng** nếu hai vòng sửa không đảo ngược |

**Chỉ số theo dõi nhưng không dùng để quyết định:**

| Chỉ số | Vì sao chỉ làm bối cảnh |
| --- | --- |
| Số tài khoản đăng nhập, số câu hỏi | Đo hoạt động, không đo giá trị; tăng được mà chất lượng không đổi |
| Thời gian tiết kiệm **tự khai** | Dùng để đối chiếu với W1 từ log, không thay W1 |
| **U1** Tỷ lệ lượt tra cứu trong Q1–Q3 có dùng trợ lý | Cho biết có đi vào quy trình không; **không** là điều kiện qua gate vì tăng U1 khi P1, P2 thấp chỉ làm tăng câu trả lời không đáng tin |

**Thiết kế đo:**

- **Nhóm đối chứng:** một ca hoặc nhóm tương đương không dùng quy trình mới. Số liệu thời gian và kết quả so sánh pilot với đối chứng, không so với niềm tin.
- **Ước tính thận trọng:** dùng median, bỏ ngoại lệ, báo khoảng chứ không báo một con số đẹp.
- **Mốc đầu:** đo trong tuần 1, ghi rõ ai đo, mẫu bao nhiêu, đo bằng nguồn nào. Không đặt mục tiêu cho chỉ số mà nhóm không lấy được số.

**Mapping năm tầng:** tầng 1 (U1) · tầng 2 (W3) · tầng 3 (W1) · tầng 4 (P1, P2, W2, P3) · tầng 5 (B1). Nền đáy: P4.

---

## 7. Kiểm tra chéo: v1 → v2

### 7.1 Dashboard v1 (nộp ở checkpoint phút 80)

Bản v1 là mẫu 4.5 điền cho tình huống này:

| Chỉ số | Mốc đầu | Mục tiêu | Nguồn dữ liệu | Phụ trách | Khi chỉ số xấu |
| --- | --- | --- | --- | --- | --- |
| Mức dùng theo quy trình | Đo tuần 1 | Mục tiêu nhóm | Log quy trình | Trưởng nhóm | Tìm điểm vướng |
| Thời gian xử lý | Đo hiện trạng | Mục tiêu nhóm | Log tác vụ | Chủ quy trình | Xem lại cách làm |
| Tỷ lệ có nguồn | Đo mẫu | Mục tiêu nhóm | Kiểm tra mẫu | Phụ trách QA | Tăng kiểm soát |
| Kết quả nghiệp vụ | Số hiện tại | Mục tiêu nhóm | Hệ thống nghiệp vụ | Chủ nghiệp vụ | Điều chỉnh / dừng |
| Rủi ro / bàn giao | Ghi hiện trạng | Ngưỡng nhóm | Log lỗi | Phụ trách AI | Bổ sung xử lý |

Lộ trình v1: 30 ngày triển khai trích nguồn · 60 ngày pilot · 90 ngày đánh giá, chuyển giai đoạn theo mốc ngày. TO-BE v1: chèn thêm bước "hỏi AI" vào quy trình cũ.

### 7.2 Góp ý và thay đổi

> **Nguồn các góp ý dưới đây:** phản biện theo bốn trục của mục 4.6 và bảng lỗi thường gặp (5.3) áp lên v1. **Đây chưa phải góp ý của nhóm khác.** Khi đổi nhóm, ghi góp ý thật vào 7.3 và chỉnh lại bảng này nếu khác.

| # | Trục | Góp ý cụ thể về v1 | Thay đổi trong v2 |
| --- | --- | --- | --- |
| 1 | Chỉ số | Cột "Mục tiêu" chỉ ghi "mục tiêu nhóm" và cột "Khi xấu" chỉ là cụm chung ("Tìm điểm vướng", "Tăng kiểm soát"): không nói được **xấu là bao nhiêu và làm gì, trong bao lâu** | Mỗi chỉ số có mục tiêu (đề xuất), ngưỡng kích hoạt, hành động cụ thể, người làm và thời hạn (mục 6) |
| 2 | Chỉ số | "Mức dùng theo quy trình" đứng đầu bảng và là điều kiện chuyển giai đoạn: thưởng cho việc dùng nhiều dù trả lời chưa đáng tin | Hạ xuống thành chỉ số bối cảnh U1; gate dựa trên tầng 4–5 và hành vi (mục 5, 6) |
| 3 | Chỉ số | Thời gian xử lý không có nhóm so sánh; "đo hiện trạng" không nói ai đo, mẫu bao nhiêu | Thêm nhóm đối chứng, dùng median từ log, ghi mẫu và người đo; tự khai chỉ để đối chiếu (mục 6) |
| 4 | Hành động | Lộ trình chuyển theo ngày, thiếu dấu hiệu hoàn thành và owner mỗi giai đoạn: thành danh sách việc | Mỗi giai đoạn có owner; hai gate theo bằng chứng; giai đoạn 3 kết thúc bằng quyết định (mục 5) |
| 5 | Framework | TO-BE chỉ chèn bước "hỏi AI", chưa nói ai kiểm chứng, ai chịu trách nhiệm, AI không chắc thì sao | Thêm chia việc Mollick, ba thay đổi bắt buộc và chuỗi tin cậy có owner (mục 4) |

### 7.3 Góp ý thật từ nhóm phản biện ⏳

| Nhóm phản biện | Trục | Góp ý | Nhóm có nhận không? | Thay đổi |
| --- | --- | --- | --- | --- |
| ⏳ | ⏳ | ⏳ | ⏳ | ⏳ |
| ⏳ | ⏳ | ⏳ | ⏳ | ⏳ |

---

## 8. Quyết định

**Quyết định hiện tại (14/10/2026): SỬA.** Tiếp tục với pilot nhỏ để sửa độ tin cậy và quy trình **trước**; chưa mở rộng và chưa dùng lượt dùng làm thước đo thành công.

**Quy tắc quyết định tại ngày 90:**

| Quyết định | Khi nào |
| --- | --- |
| **Tiếp tục / mở rộng** | P1, P2 đạt mục tiêu · W3 đạt mục tiêu · B1 cải thiện so với đối chứng và giữ được 4 tuần · không có lỗi sai nghiêm trọng đang tồn tại |
| **Sửa** | Tầng 3 đạt nhưng tầng 4 chưa đạt; hoặc đã xác định được nguyên nhân và còn một vòng sửa; hoặc thiếu owner/dữ liệu để đo |
| **Dừng** | Sau hai vòng sửa, tầng 4 vẫn không đạt; hoặc B1 xấu hơn đối chứng; hoặc chi phí vận hành lớn hơn giá trị đo được |

---

## 9. Năm câu tự kiểm

- [x] 1. **AI đi vào quy trình nào?** Q1 tra cứu · Q2 tóm tắt · Q3 kiểm chứng và báo lỗi (mục 1)
- [x] 2. **Nguyên nhân gốc nằm ở đâu?** RC1 độ tin cậy · RC2 workflow và chia việc (3.4)
- [x] 3. **Framework nào giúp trả lời?** Gartner-Lite cho readiness (3.2) · ADKAR cho người dùng (3.3) · Mollick cho chia việc (4.3)
- [x] 4. **Chỉ số nào chứng minh giá trị?** P1, P2 (tin cậy) · W1, W2 (quy trình) · B1 (nghiệp vụ) (mục 6)
- [x] 5. **Khi nào tiếp tục, sửa hoặc dừng?** Hiện tại *sửa*; quy tắc ở mục 8

---

## 10. Việc còn lại trước khi nộp ⏳

1. **Thay tình huống minh hoạ bằng tình huống thật** của nhóm (từ hoạt động mở đầu hoặc doanh nghiệp của nhóm), hoặc xác nhận tình huống này đúng với trải nghiệm của nhóm. Sửa mục 1–2 và 3.1–3.3 cho khớp.
2. **Thu bằng chứng hiện trường** (3.5): thử 20 câu hỏi, quan sát 10 lượt, phỏng vấn 3–5 người; ghi kết quả vào ô trống.
3. **Đo mốc đầu tuần 1** cho P1, P2, W1, W2, B1 và xác nhận lại các mục tiêu (đề xuất) bằng số thật.
4. **Điền tên người** cho các vai trò ở mục 5 và tên nhóm ở đầu file.
5. **Đổi nhóm phản biện thật**, ghi vào 7.3, chỉnh lại 7.2 nếu khác.
6. Kiểm tra chéo với memo: [memo-quyet-dinh.md](memo-quyet-dinh.md).

---

## Nguồn tham khảo

- OpenAI — [Morgan Stanley](https://openai.com/index/morgan-stanley/): trợ lý nội bộ cho cố vấn, khung đánh giá, mức dùng do công ty công bố.
- GOV.UK — [An Evaluation of DWP's Microsoft 365 Copilot Trial](https://www.gov.uk/government/publications/an-evaluation-of-dwps-microsoft-copilot-365-trial/an-evaluation-of-dwps-microsoft-365-copilot-trial) và [The Register](https://www.theregister.com/2026/02/04/dwp_finds_copilot_saves_civil/): so sánh nhóm dùng với nhóm không dùng, đối chiếu với nghiên cứu GDS tự khai.
- Computing — [Klarna rows back on AI](https://www.computing.co.uk/news/2025/ai/meat-back-on-the-menu-as-klarna-rows-back-on-ai) và [Entrepreneur](https://www.entrepreneur.com/business-news/klarna-ceo-reverses-course-by-hiring-more-humans-not-ai/491396): tuyển lại nhân viên sau khi chất lượng giảm.
- Khung: Prosci ADKAR · Gartner AI Maturity Model (bản rút gọn Gartner-Lite trong đề) · Mollick, *Centaurs and Cyborgs* · NIST AI RMF.
