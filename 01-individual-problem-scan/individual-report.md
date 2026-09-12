# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Đinh Ngọc Đức
- Mã học viên: 2A202602935
- Vai trò / bối cảnh (VD: sinh viên năm X, intern PM, ...): AI Engineer với 6 tháng kinh nghiệm, tham gia phát triển và vận hành các tính năng ứng dụng AI.
- Công việc hằng tuần (3-5 gạch đầu dòng để soi problem):
  - Thu thập, làm sạch và chuẩn bị dữ liệu cho các mô hình hoặc tính năng AI.
  - Phát triển và tích hợp các mô hình, API hoặc pipeline AI bằng Python.
  - Thử nghiệm prompt, mô hình và tham số để cải thiện chất lượng đầu ra.
  - Debug lỗi, theo dõi hiệu năng và kiểm tra kết quả của hệ thống AI.
  - Trao đổi yêu cầu, review code và cập nhật tiến độ với các thành viên trong nhóm.

---

## Phase 1 — Scan 5+ problems (tối thiểu 5, khuyến khích 8-10)

**Cách điền:** mỗi dòng = việc gì + ai chịu + đo bằng gì. Cột `Dấu hiệu thật` bắt buộc có số: mất bao lâu (bấm giờ mấy lần), mấy lần/tuần, bao nhiêu người gặp, log/ticket/quote nào.

> Các mốc thời gian và tần suất dưới đây là ước tính ban đầu; cần đối chiếu với time log, ticket hoặc lịch sử trao đổi trước khi nộp.

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Lặp lại / Tốn thời gian | Trước mỗi lần train, index hoặc chạy thử, phải tự đổi tên field giữa CSV/JSON, loại bản ghi trùng và kiểm tra dữ liệu thiếu vì các nguồn không cùng schema. | AI Engineer chuẩn bị dữ liệu đầu vào | Ước tính 45-60 phút/batch, 2-3 batch/tuần; nguồn kiểm chứng: notebook tiền xử lý và commit sửa schema. |
| 2 | Lặp lại / Tốn thời gian | Mỗi lần đổi prompt, model, temperature hoặc tham số retrieval, phải chạy lại cùng bộ test rồi copy score và nhận xét sang bảng theo dõi để so sánh. | AI Engineer thực hiện và báo cáo thử nghiệm | Ước tính 60-90 phút/đợt, khoảng 2 đợt/tuần; nguồn kiểm chứng: file cấu hình, output run và bảng kết quả. |
| 3 | AI có thể tốt hơn / Tốn thời gian | Sau mỗi đợt thử nghiệm, phải đọc thủ công từng câu trả lời và gắn nhãn lỗi như hallucination, thiếu bằng chứng, sai ý định hoặc trả lời không đầy đủ. | AI Engineer và người review chất lượng đầu ra | Ước tính 50 output mất khoảng 60 phút, 1-2 batch/tuần; nguồn kiểm chứng: evaluation sheet có nhãn lỗi. |
| 4 | Tốn thời gian | Khi một request trong môi trường test lỗi, phải dò cùng request ID qua tiền xử lý, retrieval/model call và hậu xử lý mới biết bước nào làm sai dữ liệu. | AI Engineer phụ trách debug pipeline | Ước tính 1-2 giờ/sự cố, 2-3 sự cố/tuần; nguồn kiểm chứng: stack trace, application log và ticket lỗi. |
| 5 | AI có thể tốt hơn / Tốn thời gian | Khi có tính năng AI mới, phải tự gom input mẫu, viết expected output và gắn tiêu chí pass/fail để tạo bộ evaluation trước khi kiểm thử. | AI Engineer và người xác nhận yêu cầu sản phẩm | Ước tính 2-3 giờ/bộ eval cho một tính năng, 1-2 lần/tháng; nguồn kiểm chứng: evaluation dataset và acceptance checklist. |
| 6 | Pain từ người khác | Ticket cho tính năng AI đôi khi thiếu input/output mẫu, metric mục tiêu và trường hợp được coi là thất bại, nên AI Engineer phải hỏi lại trước khi triển khai. | AI Engineer nhận task, Product Manager và Backend Engineer liên quan | Ước tính 2-3 lượt làm rõ/task, khoảng 3 task/tuần; nguồn kiểm chứng: comment ticket và tin nhắn trao đổi yêu cầu. |
| 7 | Pain từ người khác / Lặp lại | Khi tích hợp, Backend Engineer hoặc Tester phải hỏi lại endpoint, request/response schema, error code, timeout và giới hạn model vì README, API docs và cấu hình chưa khớp nhau. | Backend Engineer, Tester và AI Engineer hỗ trợ tích hợp | Ước tính 15-20 phút/lần, 3-5 câu hỏi/tuần; nguồn kiểm chứng: tin nhắn nhóm và comment trong pull request. |
| 8 | Lặp lại / Pain từ người khác | Thành viên mới thường vướng phiên bản Python, dependency, biến môi trường, API key hoặc model config nên chưa chạy được project sau khi clone. | AI Engineer mới và người hướng dẫn onboarding | Ước tính 1-2 giờ/lần thiết lập, 1-2 lần/tháng; nguồn kiểm chứng: terminal log, issue cài đặt và câu hỏi onboarding. |
| 9 | Lặp lại / Tốn thời gian | Hai lần mỗi tuần phải mở riêng dashboard nhà cung cấp model, cloud log và application log rồi ghép số liệu cost, latency và error rate để biết hệ thống có bất thường không. | AI Engineer tổng hợp số liệu và Tech Lead nhận cảnh báo | Ước tính 30-45 phút/lần, 2 lần/tuần; nguồn kiểm chứng: dashboard cost, latency log và error log. |
| 10 | Lặp lại / Tốn thời gian | Trước buổi cập nhật tuần, phải gom commit đã merge, ticket đã xử lý, kết quả thử nghiệm và blocker rồi viết lại thành báo cáo tiến độ cho quản lý. | AI Engineer viết cập nhật và quản lý theo dõi tiến độ | Ước tính 30-45 phút/lần, 1 lần/tuần; nguồn kiểm chứng: Git history, task board, experiment sheet và báo cáo đã gửi. |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: Gợi ý thêm problem theo 4 lăng kính cho AI Engineer có 6 tháng kinh nghiệm, kèm actor, workflow sơ bộ và cách đo; không đề xuất trợ lý AI toàn năng.
- Ý dùng được: Các pain gắn với chuẩn bị dữ liệu, theo dõi thử nghiệm, đánh giá output, debug pipeline, tạo bộ evaluation, làm rõ yêu cầu, bàn giao tích hợp, cài môi trường, theo dõi vận hành và báo cáo tiến độ.
- Ý bỏ vì không phải pain thật: Các ý quá rộng như xây agent tự quản lý toàn bộ dự án, tự thay người review hoặc tự quyết định chất lượng sản phẩm.

**Self-check Phase 1:**
- [ ] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể
- [ ] Dùng ít nhất 3/4 lăng kính
- [ ] Không có dòng chung chung kiểu "mất nhiều thời gian"

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Đọc và gắn nhãn lỗi thủ công cho output AI sau mỗi đợt thử nghiệm | Xảy ra 1-2 lần/tuần; actor và batch 50 output rõ; bottleneck đọc đối chiếu từng output đo được; AI chỉ hỗ trợ phân loại nên vẫn giữ được human review. | Batch 50 output có đại diện đủ không; cần đo mức đồng thuận giữa AI và người review. |
| 2 | Dò request lỗi qua log của nhiều bước trong pipeline | Mỗi sự cố mất 1-2 giờ; workflow debug có request ID và các chặng rõ; dễ so sánh structured logging, workflow hỗ trợ và AI. | Chưa rõ bao nhiêu thời gian mất do log thiếu cấu trúc và bao nhiêu do lỗi code thật; có thể Rule đã giải quyết phần lớn. |
| 3 | Tạo evaluation dataset thủ công cho tính năng AI mới | Tốn 2-3 giờ/tính năng; đầu vào, đầu ra và người review xác định được; có thể đo thời gian cùng tỷ lệ test case được chấp nhận. | Cần người hiểu domain để xác nhận expected output; số lần phát sinh chỉ khoảng 1-2 lần/tháng. |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — Đánh giá và gắn nhãn lỗi output AI

```text
Problem 1 câu:
Sau mỗi lần thay đổi prompt, model hoặc retrieval, AI Engineer mất khoảng 60 phút để đọc và gắn nhãn lỗi cho 50 output trước khi quyết định phiên bản có đủ chất lượng hay không.

Actor:
AI Engineer chịu trách nhiệm đánh giá chất lượng đầu ra trước khi merge hoặc bàn giao.

Thời điểm / bối cảnh:
Sau mỗi đợt thử nghiệm, khoảng 1-2 lần/tuần, trước khi chọn cấu hình hoặc phiên bản tiếp theo.

Current workflow 3-7 bước:
1. Xuất 50 input, output và evidence của đợt thử nghiệm.
2. Đọc và đối chiếu từng output với input, evidence và expected behavior.
3. Gắn loại lỗi và mức độ nghiêm trọng cho từng output.
4. Tổng hợp số lượng lỗi cùng các ví dụ điển hình.
5. Người review quyết định pass/fail cho phiên bản.

Bottleneck:
Bước 2 mất khoảng 35 phút vì người review phải đọc đủ ba phần input-output-evidence cho từng mẫu và tự phát hiện lỗi ngữ nghĩa.

Impact:
Mất khoảng 60-120 phút/tuần và làm chậm vòng lặp thử nghiệm. Nếu review vội, hallucination hoặc lỗi thiếu bằng chứng có thể lọt sang bước tích hợp.

Success metric:
Giảm thời gian review 50 output từ khoảng 60 phút xuống tối đa 35 phút; AI và người review đồng thuận ít nhất 90% trên bộ mẫu được gắn nhãn kép; không có lỗi nghiêm trọng bị AI bỏ sót trong mẫu audit ngẫu nhiên.

Non-AI alternative:
Dùng taxonomy lỗi cố định, checklist, spreadsheet có dropdown và script tự tổng hợp; người review vẫn đọc đủ 50 output nhưng giảm thao tác ghi nhãn và đếm lỗi.

AI hypothesis:
AI chỉ xử lý dữ liệu được phép sử dụng để gợi ý loại lỗi, mức độ và ưu tiên mẫu cần xem; người thật kiểm tra lại, AI không được tự quyết định pass/fail.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII / Mermaid / ảnh đính kèm):

```text
CURRENT STATE — 60 phút / 50 output

[1 Xuất và căn dữ liệu: 5']
→ [2 Đọc input-output-evidence: 35']  <-- bottleneck
→ [3 Gắn nhãn lỗi: 10']
→ [4 Tổng hợp lỗi: 5']
→ [5 Người review chốt pass/fail: 5']

FUTURE STATE — 35 phút / 50 output

[1 Script xuất dữ liệu chuẩn: 3']
→ [2 AI gợi ý nhãn + ưu tiên: 5']
→ [3 Người review mọi mẫu bị flag + 20% mẫu không bị flag: 20']  <-- human boundary
→ [4 Tự động tổng hợp: 2']
→ [5 Người review chốt pass/fail: 5']

Fallback: độ đồng thuận dưới 90% hoặc có lỗi nghiêm trọng trong mẫu audit → bỏ nhãn AI và review thủ công đủ 50 output trên cùng file đã xuất.
```
```

---

#### Problem Card #2 — Dò nguyên nhân lỗi qua log của pipeline AI

```text
Problem 1 câu:
Khi một request trong pipeline AI bị lỗi, AI Engineer mất khoảng 100 phút từ lúc tái hiện, ghép log nhiều chặng đến khi sửa và xác nhận lại kết quả.

Actor:
AI Engineer chịu trách nhiệm debug pipeline trong môi trường test hoặc deploy.

Thời điểm / bối cảnh:
Khi output sai, request timeout hoặc một bước pipeline báo lỗi; ước tính 2-3 sự cố/tuần.

Current workflow 3-7 bước:
1. Nhận lỗi và tái hiện request bằng input cũ.
2. Tìm log của tiền xử lý, retrieval/model call và hậu xử lý.
3. Ghép timestamp/request ID rồi dựng lại thứ tự sự kiện.
4. So sánh input-output từng chặng để khoanh vùng nguyên nhân.
5. Sửa lỗi và chạy lại request để xác nhận.

Bottleneck:
Bước 3 và 4 mất khoảng 50 phút vì log nằm rời rạc, format không đồng nhất và thông báo lỗi chưa chỉ ra chặng gây sai dữ liệu.

Impact:
Mỗi sự cố chiếm khoảng 1-2 giờ; với 2-3 sự cố/tuần, thời gian phát triển tính năng bị gián đoạn 2-6 giờ và người tích hợp phải chờ bản sửa.

Success metric:
Giảm toàn bộ chu kỳ debug từ khoảng 100 phút xuống tối đa 50 phút và thời gian xác định đúng chặng gây lỗi từ khoảng 80 phút xuống tối đa 25 phút; không tăng số ticket bị mở lại do chẩn đoán sai trong 24 giờ sau khi sửa.

Non-AI alternative:
Chuẩn hóa structured log, dùng một trace ID xuyên suốt pipeline và tập trung log vào một dashboard có filter theo request.

AI hypothesis:
Chỉ cân nhắc AI tóm tắt trace nếu structured logging vẫn chưa giảm đủ thời gian đọc log; chưa cần AI trong pilot đầu tiên.

Quick gut:
[ ] No AI / process fix
[x] Rule
[ ] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — khoảng 100 phút / sự cố

[1 Tái hiện request: 15']
→ [2 Tìm log ở từng chặng: 15']
→ [3 Ghép trace + dựng timeline: 30']  <-- bottleneck
→ [4 Khoanh vùng nguyên nhân: 20']
→ [5 Sửa và chạy lại: 20']

FUTURE STATE — khoảng 45 phút / sự cố

[1 Structured log tự gom theo trace ID: 5']  -- Rule
→ [2 Dashboard dựng timeline + đánh dấu error/timeout: 5']  -- Rule
→ [3 Engineer kiểm raw log + input/output: 15']  <-- human boundary
→ [4 Sửa và chạy lại: 20']

Fallback: dashboard gom log lỗi hoặc không hoạt động → lọc raw log của từng service theo trace ID và debug theo workflow cũ.
```

---

#### Problem Card #3 — Tạo evaluation dataset cho tính năng AI mới

```text
Problem 1 câu:
Khi có tính năng AI mới, AI Engineer mất khoảng 150 phút để gom input mẫu, viết expected output và tiêu chí pass/fail trước khi có thể đánh giá model.

Actor:
AI Engineer tạo bộ evaluation và người phụ trách sản phẩm xác nhận expected behavior.

Thời điểm / bối cảnh:
Trước khi thử nghiệm hoặc nghiệm thu một tính năng AI mới, khoảng 1-2 lần/tháng.

Current workflow 3-7 bước:
1. Đọc yêu cầu và làm rõ hành vi mong đợi.
2. Tìm input đại diện từ dữ liệu mẫu hoặc tình huống thực tế.
3. Viết expected output và các edge case cho từng input.
4. Viết tiêu chí pass/fail để chấm kết quả model.
5. Nhờ người phụ trách sản phẩm review rồi lưu phiên bản dataset.

Bottleneck:
Bước 3 mất khoảng 50 phút vì phải chuyển yêu cầu tự nhiên thành expected output cụ thể, đồng thời nghĩ thêm trường hợp biên nhưng không được bịa sai nghiệp vụ.

Impact:
Mỗi tính năng mất khoảng 2-3 giờ chỉ để chuẩn bị dữ liệu đánh giá; với 1-2 tính năng/tháng, việc thử model bị chậm 2-6 giờ và dễ thiếu edge case.

Success metric:
Giảm thời gian tạo một bộ eval từ khoảng 150 phút xuống tối đa 90 phút; ít nhất 80% test case AI đề xuất được người review chấp nhận mà không phải viết lại phần lớn; mỗi bộ có đủ happy path, input thiếu dữ kiện, input mơ hồ và edge case; 100% expected output được người thật duyệt.

Non-AI alternative:
Dùng template cố định, checklist loại test case và thư viện case cũ để tái sử dụng thay vì tạo lại từ đầu.

AI hypothesis:
AI tạo bản nháp input, expected output, edge case và tiêu chí pass/fail chỉ từ yêu cầu cùng case cũ đã được cung cấp; AI Engineer và người phụ trách sản phẩm phải duyệt trước khi đưa vào dataset.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — khoảng 150 phút / tính năng

[1 Đọc + làm rõ yêu cầu: 20']
→ [2 Gom input đại diện: 40']
→ [3 Viết expected output + edge case: 50']  <-- bottleneck
→ [4 Viết tiêu chí pass/fail: 25']
→ [5 Review + lưu phiên bản: 15']

FUTURE STATE — khoảng 80 phút / tính năng

[1 Template gom yêu cầu + case cũ: 10']  -- Rule
→ [2 AI draft input, expected output, edge case: 15']
→ [3 AI đề xuất tiêu chí pass/fail: 5']
→ [4 Engineer + product owner review: 45']  <-- human boundary
→ [5 Lưu phiên bản dataset: 5']

Fallback: hơn 50% case phải viết lại hoặc AI tạo case sai nghiệp vụ → bỏ batch AI và tạo thủ công từ template cùng dữ liệu gốc.
```

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Problem Card #1 — Đánh giá và gắn nhãn lỗi output AI.
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Workflow xuất hiện sau mỗi lần đổi prompt, model hoặc retrieval, khoảng 1-2 lần/tuần. Baseline là khoảng 60 phút cho 50 output; bottleneck 35 phút nằm ở bước đọc input-output-evidence, ảnh hưởng trực tiếp đến tốc độ thử nghiệm và khả năng chặn lỗi nghiêm trọng trước khi bàn giao.
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
Batch 50 output và baseline 60 phút đã đủ đại diện chưa, hay cần đo thêm qua nhiều đợt thử nghiệm? Taxonomy lỗi, checklist và sampling có thể giải quyết phần lớn pain mà chưa cần AI hay không?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: Baseline hiện là ước tính; 50 output có thể chưa đại diện; dùng AI để review AI có nguy cơ lặp lại cùng kiểu sai; taxonomy và sampling có thể đã giảm đáng kể thời gian.
- Tôi sửa gì: Giữ AI ở vai trò gợi ý nhãn và ưu tiên mẫu; thêm ngưỡng đồng thuận 90%, audit ngẫu nhiên mẫu không bị flag, non-AI alternative và điều kiện quay về review thủ công.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
