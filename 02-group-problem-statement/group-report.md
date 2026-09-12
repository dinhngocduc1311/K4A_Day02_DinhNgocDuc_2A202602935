# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-----------|-------------|---------------------------------------------------------------|
| 1 | Đoàn Tuấn Long | 2A202602609 | workflow |
| 2 | Đinh Ngọc Đức | 2A202602935 | writer |
| 3 | Nguyễn Đình Phúc | 2A202602953 | writer |
| 4 | Trần Thị Hải Yến | 2A202602663 | research |
| 5 | Nguyễn Ngọc Thái An | 2A202602462 | research |

**Candidate problem nhóm chọn (1 câu):**

Chủ hộ kinh doanh gặp khó khăn và rủi ro sai sót pháp lý khi tự kê khai thuế 01/CNKD hằng quý do thiếu hiểu biết về các trường thông tin và cách đối chiếu số liệu.

---

## Phase 3 — Group Convergence: từ 15 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Đinh Ngọc Đức | Đọc và gắn nhãn lỗi thủ công cho output AI sau mỗi đợt thử nghiệm | AI Engineer chịu trách nhiệm đánh giá chất lượng đầu ra | Đọc, đối chiếu input-output-evidence cho 50 mẫu, khoảng 35 phút/batch | Workflow và metric rõ; cần kiểm chứng batch 50 mẫu có đại diện và AI có bỏ sót lỗi nghiêm trọng không. |
| 2 | Đinh Ngọc Đức | Dò request lỗi qua log của nhiều bước trong pipeline AI | AI Engineer phụ trách debug pipeline | Ghép trace và khoanh vùng nguyên nhân giữa tiền xử lý, retrieval/model call và hậu xử lý, khoảng 50 phút/sự cố | Pain kỹ thuật rõ nhưng structured logging theo trace ID có thể đã đủ, chưa chắc cần AI. |
| 3 | Đinh Ngọc Đức | Tạo evaluation dataset thủ công cho tính năng AI mới | AI Engineer và người phụ trách sản phẩm duyệt expected behavior | Viết expected output và edge case từ yêu cầu, khoảng 50 phút/bộ eval | Scope gọn, đo được; cần người hiểu domain và tần suất chỉ 1-2 lần/tháng. |
| 4 | Nguyễn Đình Phúc | Soạn tin nhắn báo cáo cho sếp sau mỗi lần đẩy build mới lên TestFlight | Mobile Developer và người quản lý nhận build | Lọc commit liên quan rồi viết tóm tắt thay đổi dễ hiểu, khoảng 15 phút/lần | Lặp 1-2 lần/ngày, pilot dễ; rủi ro commit thiếu context và văn phong AI không phù hợp. |
| 5 | Nguyễn Đình Phúc | Tự phân bổ lịch ôn từ vựng theo spaced repetition | Người học tiếng Anh tự quản lý lịch ôn | Tính ngày ôn tiếp theo và sắp lại danh sách từ mỗi ngày, khoảng 20-30 phút | Rule rất rõ và app như Anki có thể đã giải đủ; giá trị bổ sung của AI còn yếu. |
| 6 | Nguyễn Đình Phúc | Sếp hoặc Tester báo app crash bằng ảnh/video nhưng không kèm log và bước tái hiện | Mobile Developer nhận lỗi; sếp/Tester chờ bản sửa | Tái hiện lỗi và khoanh vùng code khi đầu vào chỉ có ảnh/video, mất 1-2 giờ/lần | Pain lớn nhưng thiếu dữ liệu gốc; cần sửa quy trình thu thập crash log trước khi nghĩ đến AI multimodal. |
| 7 | Trần Thị Hải Yến | Bắt đúng thời điểm và Sequence/Acknowledgment number để inject gói trong bài lab TCP Hijacking | Sinh viên thực hiện demo trong môi trường Labtainer được kiểm soát | Khớp seq/ack trước khi hai đầu tiếp tục giao tiếp; tỷ lệ thất bại ước tính khoảng 70% | Problem rất cụ thể và đo được nhưng domain hẹp; cần tách ảnh hưởng của latency khỏi lỗi logic trước khi chọn giải pháp. |
| 8 | Trần Thị Hải Yến | Viết cấu hình mô phỏng mạng để đóng gói bài thực hành Labtainer | Sinh viên dựng lab và GVHD nghiệm thu | Tra cú pháp rồi ánh xạ topology giữa các container, mất khoảng 3-4 ngày/bài | Workflow rõ nhưng có thể giải phần lớn bằng template và tài liệu chuẩn; cần kiểm tra tài nguyên có sẵn. |
| 9 | Trần Thị Hải Yến | Chụp terminal, xuất log Wireshark và căn chỉnh vào Word để báo cáo tiến độ | Sinh viên viết báo cáo và GVHD đọc kết quả | Cắt ghép ảnh, log rồi căn chỉnh thủ công, mất 2-3 giờ mỗi thứ Sáu | Lặp lại và định lượng tốt; Rule/script hoặc đổi định dạng báo cáo có thể đủ, AI chưa chắc cần thiết. |
| 10 | Đoàn Tuấn Long | Tự kê khai thuế 01/CNKD hằng quý | Chủ hộ kinh doanh tự chuẩn bị và nộp tờ khai | Hiểu đúng từng trường rồi đối chiếu số liệu doanh thu, chứng từ trước khi nộp | Impact cao và workflow tuyến tính; thông tin pháp lý, biểu mẫu và khác biệt địa phương phải được kiểm chứng từ nguồn chính thức. |
| 11 | Đoàn Tuấn Long | Phân biệt deepfake hoặc cuộc gọi lừa đảo khi đang nghe máy | Người dùng điện thoại, đặc biệt người ít kinh nghiệm số | Đánh giá danh tính và dấu hiệu lừa đảo trong thời gian thực khi bị thúc ép | Impact tiềm năng lớn nhưng scope rộng, false positive nguy hiểm và metric ngoài thực tế khó đo trong lab. |
| 12 | Đoàn Tuấn Long | Xác định checklist hồ sơ hoàn tiền khi mua thuốc ngoài bệnh viện | Người tham gia BHYT hoặc người nhà chuẩn bị hồ sơ | Xác định đúng điều kiện và giấy tờ cần gom trước khi nộp, ước tính 45-90 phút/lần | Bài toán gọn nhưng baseline chưa được xác nhận; quy trình và điều kiện hưởng cần kiểm chứng từ nguồn chính thức. |
| 13 | Nguyễn Ngọc Thái An | Lọc và đối chiếu JD trước khi ứng tuyển | Người tìm việc nộp nhiều vị trí | Đọc từng yêu cầu rồi so với hồ sơ để phát hiện mismatch trước khi apply | Workflow rõ và pilot dễ; tỷ lệ mismatch khoảng 30% mới là ước tính, cần kiểm tra lại trên 10 lần apply. |
| 14 | Nguyễn Ngọc Thái An | Trả lời Situational Judgement Test khi competency chấm điểm bị ẩn | Ứng viên tham gia chương trình tuyển dụng có SJT | Suy ra competency và tiêu chí chấm từ tình huống khi không có ground truth | Insight tốt nhưng khó validate vì tiêu chí tuyển dụng không công khai và có thể chỉ đúng với một vài chương trình. |
| 15 | Nguyễn Ngọc Thái An | Tailor CV cho từng job hoặc chương trình ứng tuyển | Người tìm việc ứng tuyển nhiều vị trí | Ánh xạ kinh nghiệm thật vào yêu cầu JD rồi chỉnh nội dung CV, mất 20-30 phút/lần | Tần suất và metric rõ; cần tách pain do thiếu công cụ khỏi quy trình cá nhân chưa chuẩn hóa và không được bịa kinh nghiệm. |

### 3.2. Gom trùng / cluster (gom 15 ý thành 3-4 cụm)

> Nhóm theo pattern của workflow và bottleneck, không nhóm theo ngành hoặc theo loại công nghệ, để tránh chọn solution trước khi hiểu problem.

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A — Kiểm thử và chẩn đoán hệ thống kỹ thuật | #1 Gắn nhãn lỗi output AI; #2 Dò log pipeline AI; #3 Tạo evaluation dataset; #6 Tái hiện app crash thiếu log; #7 Debug TCP Hijacking | Người làm kỹ thuật phải đọc output, evidence, log hoặc hành vi chạy thử để tìm lỗi, xác định nguyên nhân hay quyết định hệ thống đạt yêu cầu chưa. Bottleneck nằm ở khâu đối chiếu nhiều tín hiệu rời rạc. | Có workflow và metric tương đối rõ, nhưng input giữa các bài rất khác nhau. Cần chọn một candidate cụ thể thay vì cố xây công cụ debug chung cho cả cluster. |
| B — Chuẩn hóa tài liệu và bàn giao kỹ thuật | #4 Báo cáo sau khi đẩy build TestFlight; #8 Viết cấu hình Labtainer; #9 Chụp terminal và log Wireshark vào Word | Người thực hiện phải gom artifact kỹ thuật từ code, terminal hoặc công cụ mạng rồi chuyển thành nội dung/cấu hình có cấu trúc để người khác sử dụng hoặc đánh giá. | Lặp lại và dễ pilot; template, script hoặc đổi định dạng bàn giao có thể giải phần lớn pain trước khi cần AI. |
| C — Lập kế hoạch và đối chiếu tiêu chí cá nhân | #5 Lập lịch ôn spaced repetition; #13 Đối chiếu JD; #14 Giải mã competency SJT; #15 Tailor CV | Người dùng phải so trạng thái hoặc hồ sơ hiện tại với lịch, yêu cầu hay tiêu chí đánh giá để quyết định bước tiếp theo hoặc điều chỉnh nội dung. | Độ mơ hồ không đồng đều: spaced repetition có Rule rõ, còn JD/SJT/CV cần hiểu ngữ cảnh. Phải kiểm tra giải pháp có sẵn và tránh để AI bịa tiêu chí hoặc kinh nghiệm. |
| D — Quyết định có rủi ro pháp lý, sức khỏe hoặc an toàn | #10 Kê khai thuế 01/CNKD; #11 Nhận diện deepfake/lừa đảo qua điện thoại; #12 Checklist hoàn tiền thuốc theo BHYT | Người dùng thiếu thông tin đáng tin cậy để ra quyết định đúng trong tình huống có hậu quả tài chính, pháp lý hoặc an toàn. | Impact cao nhưng sai sót khó chấp nhận; cần nguồn chính thức, validation thật và human boundary chặt. Scope hiện rộng hơn khả năng kiểm chứng nhanh trong lab. |

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| #4 — Soạn tin nhắn báo cáo cho sếp sau mỗi lần đẩy build TestFlight | Actor và trigger rõ: Mobile Developer, ngay sau mỗi lần đẩy build; lặp 1-2 lần/ngày và baseline khoảng 15 phút/lần. Bottleneck tập trung ở lọc commit rồi chuyển thành nội dung dễ hiểu. Có dữ liệu pilot sẵn từ commit history, build cũ và tin nhắn đã gửi; so sánh được template/Rule với AI Workflow. | Commit message có thể thiếu context hoặc chứa thông tin kỹ thuật nhạy cảm. Cần xác nhận sếp có chấp nhận format/văn phong mới và target 3 phút có tính cả thời gian kiểm tra hay không. |
| #10 — Tự kê khai thuế 01/CNKD hằng quý | Actor rõ (chủ hộ kinh doanh) và workflow tuyến tính (gom chứng từ, đối chiếu số liệu, điền biểu mẫu). Impact tiềm năng cao khi giúp giảm thiểu sai sót và tiết kiệm thời gian cho người không có chuyên môn kế toán. | Rủi ro pháp lý và tài chính cao nếu có sai sót. Yêu cầu thông tin pháp lý phải chính xác và được cập nhật từ nguồn chính thức. Scope rộng và khó thực hiện validation đủ chặt trong môi trường lab. |
| #9 — Chụp terminal, xuất log Wireshark và căn chỉnh Word cho báo cáo tuần | Actor, lịch xảy ra và output đều rõ: sinh viên làm báo cáo cho GVHD mỗi thứ Sáu. Baseline 2-3 giờ/tuần và các bước chạy lệnh, chụp ảnh, xuất log, format Word dễ vẽ before/after. Có thể pilot trên một báo cáo và so sánh process fix, script/Rule với Workflow hỗ trợ tóm tắt. | Cần xác nhận GVHD có bắt buộc file Word, ảnh chụp và format của trường không. Chưa rõ phần tốn thời gian nhất là thu thập bằng chứng hay căn chỉnh; nếu chỉ là format thì Rule/script có thể đủ, không cần AI. |

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #10 — Tự kê khai thuế 01/CNKD hằng quý | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **35/35** |
| #4 — Báo cáo sau khi đẩy build TestFlight | 5 | 5 | 4 | 5 | 5 | 5 | 5 | **34/35** |
| #9 — Làm báo cáo lab từ terminal/Wireshark | 5 | 5 | 4 | 5 | 5 | 4 | 5 | **33/35** |

Giải thích điểm chưa tối đa: #10 đã được nhóm thảo luận kỹ và tìm ra cách thu hẹp scope để hoàn toàn khả thi trong lab nên đạt điểm tối đa; #4 chưa có xác nhận của sếp nên evidence là 4/5; #9 có khả năng chỉ cần template/script nên khả năng so sánh đủ ba mức Rule/Workflow/Agent là 4/5.

**Candidate nhóm chọn (1 bài duy nhất):**

```text
#10 — Tự kê khai thuế 01/CNKD hằng quý.
```

**Vì sao chọn (4-5 câu):**

```text
Candidate #10 giải quyết một bài toán có impact cực kỳ lớn đối với các chủ hộ kinh doanh, giúp họ tránh rủi ro pháp lý và tiết kiệm thời gian đáng kể. Workflow của bài toán mang tính tuyến tính (gom chứng từ -> đối chiếu số liệu -> điền form), rất phù hợp để xây dựng công cụ AI hỗ trợ từng bước. Dù ban đầu lo ngại về rủi ro pháp lý, nhóm đã thống nhất thu hẹp scope (chỉ hỗ trợ một số biểu mẫu phổ biến hoặc xử lý mô phỏng) để có thể triển khai an toàn và hiệu quả trong thời gian lab. Việc so sánh giữa Rule (dùng template cố định) và AI (xử lý logic phức tạp, giải thích luật) cũng rất nổi bật, tạo đất diễn tốt cho một Agent thực sự.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

```text
#4 — Báo cáo sau đẩy build TestFlight: Bài toán rõ ràng và dễ làm, nhưng độ phức tạp và impact mang lại không cao bằng bài toán thuế. Ngoài ra, việc sếp có chấp nhận văn phong của AI hay không vẫn là một rào cản cần xác nhận.

#9 — Làm báo cáo lab: Workflow thủ công tốn thời gian (2-3 giờ/tuần), tuy nhiên phần lớn có thể được giải quyết bằng các script/template định dạng có sẵn mà chưa chắc cần đến một Workflow AI phức tạp.
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

```text
Chưa có dữ liệu về disagreement thật trong phần nhóm đã cung cấp. Nhóm cần chấm độc lập ba candidate, thảo luận các tiêu chí lệch từ 2 điểm trở lên và ghi lại ý kiến cùng cách chốt nếu có bất đồng.
```

---

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

Nhóm làm micro poll với 8 bạn trong lớp có người thân hộ kinh doanh, rồi đối chiếu với 3 nguồn quote công khai. Chưa phỏng vấn trực tiếp chủ hộ tại cửa hàng; chưa bấm giờ lần kê thật.

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn) | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview (nguồn thứ cấp — lãnh đạo thuế / địa phương, không phải chủ hộ tự nói với nhóm) | 3 nguồn quote | Phó Cục trưởng Mai Sơn: nhiều hộ “lo kê khai sai, chưa nắm chắc quy định, nộp thuế chưa đúng hoặc lo ngại bị xử phạt”. Lãnh đạo tỉnh Bắc Ninh: bốn khó khăn gồm “tâm lý ngại thay đổi và e ngại minh bạch doanh thu; kỹ năng số hạn chế; chưa lựa chọn được giải pháp phù hợp; lo ngại chi phí ban đầu và an toàn dữ liệu”. Đại lý thuế DHTaxLaw ghi nhận hộ hay “không biết chọn phương pháp tính thuế; sai sót khi kê khai online; không cập nhật quy định mới”. | Quote đến từ cơ quan hỗ trợ / dịch vụ thuế, có thể phóng đại pain để biện minh chương trình hỗ trợ. Chưa có thời gian tự kê khai đo bằng đồng hồ từ 1 chủ hộ. | Thu hẹp actor: hộ vừa chuyển từ khoán sang kê khai, doanh thu khoảng 500 triệu–3 tỷ, nộp theo quý. Không giải “minh bạch doanh thu / sợ bị thanh tra”. |
| Survey / poll (hỏi nhanh 8 bạn trong lớp có người thân hộ KD) | 8 | 6/8 người thân phải kê 01/CNKD quý 1/2026; 5/8 chọn “điền chỉ tiêu / không biết ô nào” là bước đau nhất; 4/8 ước lần đầu mất ~2–4 giờ; 3/8 gia đình thuê đại lý ~500K–1 triệu/quý. Mức đáng giải: trung bình 4,1/5. Quote: “Bố em mở eTax được rồi nhưng ngồi đoán ô doanh thu theo ngành gần một tiếng”; “Mẹ em bảo sợ kê sai nên đưa hết hóa đơn cho cô kế toán”; “Khó nhất là cộng 3 tháng bán tạp hóa với bán online cho đúng ngành”. | 2/8 không đau: 1 hộ DT dưới ngưỡng, 1 đã thuê đại lý từ đầu nên “không đụng form”. 1 bạn nói pain thật là đăng nhập VNeID, không phải hiểu field. Thời gian 2–4 giờ là nhớ lại, không bấm giờ. | Giữ bottleneck ở hiểu field + cộng DT theo ngành, không làm nút nộp. Loại hộ đã thuê đại lý thường xuyên khỏi actor. Không giải bài VNeID (1/8). Baseline lab lấy ~2,5–4 giờ lần đầu, không khẳng định 3–5 giờ cho mọi hộ. |
| Log / review / chương trình hỗ trợ | Bắc Ninh 106.537 hộ; Tổ xung kích 1.220 hộ được hướng dẫn; “Bình dân học vụ kê khai” tiếp cận >1 triệu hộ, giải đáp >3.000 câu hỏi | Bắc Ninh: mới >2.000 hộ dùng phần mềm bán hàng (**chưa đến 2%**); phần lớn vẫn sổ sách thủ công. Cục Thuế phải “cầm tay chỉ việc” và mở Cổng trải nghiệm vì hộ thiếu công cụ, kỹ năng, chưa quen kê khai điện tử. 3.000 câu hỏi trong 1 tuần cho thấy vướng mắc lặp lại khi lập tờ khai. | Số liệu Bắc Ninh không đại diện cả nước. 3.000 câu hỏi gồm cả đăng ký tài khoản / VNeID, không chỉ điền 01/CNKD. | Tách bước “đăng nhập eTax / VNeID” (process/Rule) khỏi bước “hiểu chỉ tiêu + chọn phương pháp TNCN + đối chiếu doanh thu” (đáng hỗ trợ). |

Nguồn quote / số liệu:
- [Bắc Ninh TV — Cổng trải nghiệm kê khai](https://bacninhtv.vn/tin-tuc/4/189976/ra-mat-cong-trai-nghiem-dong-hanh-ho-kinh-doanh-chuyen-sang-ke-khai-thue)
- [Nhân Dân — Bắc Ninh hỗ trợ 10.000 hộ CĐS](https://nhandan.vn/bac-ninh-thi-diem-ho-tro-10000-cua-hang-ho-kinh-doanh-chuyen-doi-so-post983125.html)
- [BNEWS — Tổ xung kích Bắc Ninh](https://bnews.vn/to-xung-kich-bac-ninh-thuc-day-ho-kinh-doanh-chuyen-doi-so-trong-nop-thue/387365.html)
- [Bắc Ninh TV — Bình dân học vụ kê khai](https://bacninhtv.vn/tin-tuc/4/194296/binh-dan-hoc-vu-cac-don-vi-cam-tay-chi-viec-cho-ho-kinh-doanh-khai-thue)
- [DHTaxLaw — khó khăn khi khai Q1/2026](https://www.dhtaxlaw.com.vn/huong-dan-khai-thue-quy-1-2026-cho-ho-kinh-doanh-tu-500-trieu-den-3-ty-tren-dich-vu-cong)

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

```text
Poll 8 bạn: 6/8 người thân phải kê 01/CNKD; pain lặp lại ở hiểu field và cộng DT theo ngành, không phải cổng nộp (5/8). 2/8 không đau vì dưới ngưỡng hoặc đã thuê đại lý — khớp insight nguồn công khai. Nhóm thu hẹp: không làm “nộp thuế hộ”, không làm hộ đã có đại lý; chỉ hỗ trợ giải thích field + checklist chứng từ, chủ hộ tự nộp.
```

Bằng chứng đính kèm (nếu có): `02-group-problem-statement-survey.png`, `...-interview-notes.md`

Giả định chưa chắc: 2–4 giờ/lần đầu lấy từ nhớ lại của 4/8 bạn, chưa bấm giờ với chủ hộ tại cửa hàng.

### 4.2. Research giải pháp đã có (ít nhất 2-3 tools/patterns + 1-2 link kiểm được)

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| eTax Mobile + Cổng DVC thuế (mã TTHC 1.011022) | [Google Play eTax Mobile](https://play.google.com/store/apps/details?id=com.etax.icanhan); nộp tờ khai: [dichvucong.gdt.gov.vn](https://dichvucong.gdt.gov.vn/tthc/homelogin) | Đăng nhập VNeID, chọn kỳ, nhập doanh thu, nộp 01/CNKD, OTP | Kênh nộp chính thức, miễn phí, đã có trên điện thoại | Không giải thích chỉ tiêu [01a]/[01b]/[01c]; không gom hóa đơn; hướng dẫn Q1/2026 vẫn ~15 bước. SofiPOS: “Khó nhất khi điền 01/CNKD là phải tổng hợp doanh thu thực tế 3 tháng, tách theo từng ngành nghề.” — [sofipos.com.vn](https://sofipos.com.vn/blog/huong-dan-nop-to-khai-01-cnkd-tren-etax-mobile/) | Đừng build cổng nộp mới. AI dừng trước nút nộp. |
| HTKK 5.6.0 (Cục Thuế, 16/3/2026) | [Tải HTKK](https://www.gdt.gov.vn/wps/portal/home/hotrokekhai); [MISA hướng dẫn HTKK cho HKD](https://sme.misa.vn/342471/huong-dan-ke-khai-thue-ho-kinh-doanh-tren-htkk-moi-nhat-theo-quy-dinh/) | Lập mẫu 01/CNKD, tự tính GTGT/TNCN nếu đã nhập số, xuất XML | Chuẩn cơ quan thuế; giảm lỗi format | Vẫn cần người nhập đúng doanh thu; cài PC, không giải thích field bằng tiếng đời thường | Rule/phần mềm đủ cho tính thuế. AI nếu có thì ở bước “số liệu đầu vào đúng chưa / field này nghĩa là gì”. |
| AMIS Kế toán HKD (MISA) / Fast HKD | [amis.misa.vn](https://amis.misa.vn/amis-ke-toan-ho-kinh-doanh/); [fast.com.vn](https://fast.com.vn/phan-mem-ke-toan-fast-ho-kinh-doanh/) | Sổ sách TT 152/2025, tổng hợp số lên 01/CNKD, HĐĐT, bán hàng | Đúng mẫu TT 18/2026 rồi TT 50/2026; giảm sai sót nếu dùng đều | Phải nhập liệu suốt quý; chi phí (Fast từ ~146.000đ/tháng); hộ Bắc Ninh <2% đã dùng phần mềm bán hàng | Non-AI mạnh nếu hộ chịu dùng POS/sổ. Lab không cần clone MISA. |
| Cầm tay chỉ việc / Cổng trải nghiệm / đại lý thuế | [Cổng trải nghiệm Bắc Ninh](https://bacninhtv.vn/tin-tuc/4/189976/ra-mat-cong-trai-nghiem-dong-hanh-ho-kinh-doanh-chuyen-sang-ke-khai-thue); [Bình dân học vụ](https://bacninhtv.vn/tin-tuc/4/194296/binh-dan-hoc-vu-cac-don-vi-cam-tay-chi-viec-cho-ho-kinh-doanh-khai-thue) | Hướng dẫn tại chỗ, sandbox không phát sinh nghĩa vụ, trả lời câu hỏi | Đúng pain “sợ làm sai”; có người thật | Không scale; 1.220 hộ/tổ xung kích vs 106.537 hộ tỉnh; phụ thuộc lịch hỗ trợ | Pattern tốt cho lab: sandbox + giải thích, không nộp thay. |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
Không build Agent tự nộp 01/CNKD hay tự bịa doanh thu. Cổng nộp và HTKK đã có; phần mềm kế toán đã tổng hợp số nếu hộ nhập liệu. Khoảng trống còn lại là hộ không hiểu field, không biết chọn PP1/PP2, và không đối chiếu được chứng từ rời trước khi mở eTax. Hướng lab: Workflow hẹp — Rule/checklist danh mục chứng từ + AI giải thích chỉ tiêu / draft số từ hóa đơn mẫu — chủ hộ review rồi tự nộp trên eTax. Luật đổi nhanh (TT 18 rồi TT 50/2026 từ kỳ tháng 5/Q2), mọi câu trả lời pháp lý phải gắn link văn bản, không để model nhớ.
```

> Lưu ý: không dùng số liệu AI đưa nếu không verify được link chính thức. Ghi rõ giả định chưa chắc. Baseline thời gian 3–5 giờ/lần khai và “15 bước eTax ≈ 10 phút nếu đã có số” là claim của blog hướng dẫn, chưa đo với actor nhóm chọn.

---

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file: `02-group-problem-statement-workflow.png/pdf/md`

Scope sau Phase 4: chủ hộ vừa chuyển khoán → kê khai, doanh thu ~500 triệu–3 tỷ/năm, nộp **theo quý**, mẫu 01/CNKD. Thời gian là ước lượng lần đầu (chưa bấm giờ với chủ hộ thật).

```text
CURRENT STATE — 7 bước, ~4 giờ / quý (lần đầu)

[1 Gom hóa đơn điện tử + giấy + sổ tay: 45' - chủ hộ]
→ [2 Cộng doanh thu 3 tháng, tách theo ngành: 75']
→ [3 Chọn PP1 (% DT) hay PP2 (thu nhập) + chỉ tiêu 01a/01b/01c: 30']
→ [4 Mò field trên eTax (~15 bước), không hiểu ô nào: 60']  <-- bottleneck
→ [5 Đăng nhập VNeID / eTax + OTP nộp: 20']
→ [6 Tự rà lại số trước khi thoát: 15']
→ [7 Nếu bị trả / sợ sai → hỏi chi cục hoặc đại lý: 60'+]

Tần suất: 1 lần/quý × 4 = 4 lần/năm
Handoff: bước 7 sang cơ quan thuế hoặc đại lý thuế
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|---|---|---|---|---|---|
| 1 | Chủ hộ | Hóa đơn điện tử, hóa đơn giấy, sổ bán hàng thủ công trong quý | Chồng chứng từ chưa phân loại | ~45' / quý | Handoff từ bán hàng hằng ngày; Bắc Ninh <2% hộ có phần mềm bán hàng nên bước này nặng. |
| 2 | Chủ hộ | Chứng từ rời 3 tháng | Tổng DT theo ngành (thường ghi tay / Excel) | ~75' / quý | SofiPOS: đây là bước khó nhất khi điền 01/CNKD. Chưa phải AI-mandatory — Excel được. |
| 3 | Chủ hộ | Ngưỡng DT, ngành nghề | Quyết định PP1 hoặc PP2; chọn [01a]/[01b]/[01c] | ~30' / quý | DHTaxLaw: hộ hay không biết chọn phương pháp. Sai bước này làm sai cả tờ khai. |
| 4 | Chủ hộ | Số liệu bước 2–3 + form eTax | Tờ khai nháp, nhiều ô để trống hoặc đoán | ~60' / lần đầu | **Bottleneck chính:** ngôn ngữ chỉ tiêu ≠ tiếng đời thường; 15 bước thao tác. |
| 5 | Chủ hộ | Tài khoản VNeID / eTax, OTP | Tờ khai đã nộp | ~20' / quý | Process/cổng đã có. Không phải pain cốt lõi (Phase 4). |
| 6 | Chủ hộ | Tờ khai vừa điền | Tờ khai đã nhìn lại (thường soi hời hợt vì không biết field) | ~15' / quý | Review yếu vì thiếu checklist đối chiếu chứng từ. |
| 7 | Chủ hộ + chi cục / đại lý | Tờ khai bị trả hoặc chủ hộ không chắc | Hồ sơ nộp lại hoặc tờ khai do đại lý làm | 60'+ nếu sai; không phải mỗi quý | Handoff đắt (500K–1 triệu/quý nếu thuê). |

**Bottleneck chính (2-3 câu):**

```text
Bottleneck không nằm ở cổng nộp (bước 5) mà ở bước 3–4: chủ hộ phải tự chọn phương pháp TNCN và điền chỉ tiêu 01/CNKD khi chưa hiểu field nghĩa là gì. Bước 2 (cộng DT 3 tháng theo ngành) làm bottleneck nặng hơn vì chứng từ rời, sổ tay. Hệ quả: lần đầu mất khoảng 3–5 giờ, dễ kê sai rồi bị trả hồ sơ hoặc phải thuê đại lý.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người, boundary ở đâu, fallback khi AI sai.

```text
FUTURE STATE — 6 bước, dưới 60' lần đầu (kỳ vọng lab)

[1 Chủ hộ chụp/upload chứng từ quý: 10']           -- Người
→ [2 Checklist đủ loại chứng từ + tách ngành: 3']  -- Rule
→ [3 AI gắn nhãn HĐ, cộng DT, giải thích field,
     gợi ý PP1 nếu DT 500tr–3tỷ: 5']               -- AI (Workflow step)
→ [4 Chủ hộ đối chiếu số với HĐ/sổ, sửa ô lạ: 20'] -- Human boundary
→ [5 Chủ hộ tự nhập + nộp trên eTax: 15']          -- Người (không AI nộp)
→ [6 Lưu bản đối chiếu + link văn bản đã dùng: 5'] -- Rule / Người

Fallback:
- AI không chắc ngành / phương pháp / số thuế → hiện "chưa đủ căn cứ, hỏi chi cục hoặc đại lý"; không đoán luật.
- AI cộng sai DT → chủ hộ bỏ số AI, nhập tay từ checklist Excel.
- Tờ khai bị trả → không để AI nộp lại tự động; chủ hộ sửa theo thông báo cơ quan thuế.

Bottleneck mới (chấp nhận được): bước 4 review. Đây là điểm kiểm soát trước khi phát sinh nghĩa vụ thuế.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| Tổng thời gian | ~4 giờ / quý (lần đầu, ước lượng) | Dưới 60 phút / quý | Bấm giờ 1 kỳ mẫu (hóa đơn 1 quý) với 1 chủ hộ hoặc đóng vai trên bộ chứng từ giả |
| Số bước | 7 | 6 | Đếm bước trên sơ đồ; giảm effort chứ không tối ưu số bước |
| Số bước thủ công | 7/7 | 3/6 (chụp chứng từ, review, nộp eTax) | Bước 2 Rule; bước 3 AI; bước 6 chủ yếu lưu file |
| Bottleneck chính | Hiểu field + điền eTax (~60–90') | Review/đối chiếu (~20') | Thời gian bước 3–4 trước vs bước 4 sau |
| Risk mới | Kê sai vì không hiểu field, không có AI bịa số | Hallucination (sai ngành, sai PP, sai DT) | Số ô AI đánh dấu "không chắc"; số lần chủ hộ phải bỏ draft; không để AI nộp |

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field | Nội dung |
|---|---|
| **Actor** | Chủ hộ kinh doanh vừa chuyển từ thuế khoán sang kê khai, doanh thu khoảng 500 triệu–3 tỷ đồng/năm, tự làm tờ khai quý (không có kế toán nội bộ). Ví dụ: tiệm tạp hóa, quán ăn, shop bán qua Facebook/TikTok. Không gồm hộ đã thuê đại lý thuế thường xuyên hoặc hộ dùng đủ phần mềm bán hàng + kế toán. |
| **Workflow** | Cuối mỗi quý chủ hộ gom hóa đơn/sổ, cộng doanh thu 3 tháng theo ngành, chọn phương pháp TNCN và chỉ tiêu [01a]/[01b]/[01c], điền mẫu 01/CNKD trên eTax Mobile hoặc Cổng DVC, đăng nhập VNeID rồi nộp OTP. Nếu không chắc hoặc bị trả hồ sơ thì hỏi chi cục / thuê đại lý. |
| **Bottleneck** | Bước chọn phương pháp và điền chỉ tiêu (~60–90 phút lần đầu) vì ngôn ngữ form không khớp tiếng bán hàng hằng ngày. Cộng thêm bước cộng DT 3 tháng từ chứng từ rời (~75 phút) khi hộ chưa có phần mềm. Cổng nộp không phải nút nghẽn. |
| **Impact** | Lần đầu mất khoảng 3–5 giờ/quý; kê sai có thể bị truy thu, phạt hành chính (NĐ 310/2025 về chậm/sai hồ sơ). Thuê đại lý thay thế khoảng 500K–1 triệu/quý. Ở Bắc Ninh <2% hộ có phần mềm bán hàng nên pain lặp lại trên số hộ lớn, dù nhóm chưa đo được trên actor thật. |
| **Success Metric** | (1) Giảm thời gian từ lúc có chồng chứng từ đến lúc sẵn sàng nhập eTax từ ~2,5–3 giờ xuống dưới 30 phút. (2) Tổng thời gian lần đầu dưới 60 phút, kể cả nộp. (3) Không tăng số tờ khai bị trả vì sai chỉ tiêu / sai phương pháp trên bộ chứng từ pilot. Metric thời gian hiện vẫn là kỳ vọng, chưa có baseline bấm giờ. |
| **Boundary** | AI không nộp tờ khai, không ký OTP, không tự bịa doanh thu hay chọn phương pháp khi thiếu căn cứ. Chỉ dùng chứng từ chủ hộ cung cấp; mọi giải thích pháp lý phải kèm link TT 18/2026 hoặc TT 50/2026. Chủ hộ chịu trách nhiệm số liệu cuối và tự nộp trên kênh cơ quan thuế. |

**Câu hỏi AI phản biện v0 (nếu có):**
- Field nào mơ hồ: Success metric dựa trên ước lượng 3–5 giờ, chưa interview chủ hộ; ngưỡng 500 triệu vs 1 tỷ giữa các văn bản 2026 dễ lẫn; “không tăng tờ khai bị trả” khó đo trong lab vì không nộp thật.
- Tôi sửa gì: Ghi rõ baseline là giả định; thu hẹp pilot = bộ hóa đơn mẫu 1 quý + đóng vai điền form, không nộp lên hệ thống thật; tách PP1 (500tr–3tỷ) thành scope v0, chưa làm PP2.

---

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: [x] Thấp (có đúng/sai rõ) / [ ] Cao (nhiều cách trả lời vẫn OK) — Vì sao: Số doanh thu, phương pháp PP1/PP2, chỉ tiêu [01a]/[01b]/[01c] và tỷ lệ thuế theo ngành có đáp án đúng/sai theo văn bản. Phần giải thích tiếng đời thường được diễn đạt nhiều cách, nhưng output chịu trách nhiệm pháp lý phải khớp rule.
- Độ phức tạp: [ ] Thấp (1-2 bước) / [x] Cao (3+ bước/nguồn, phụ thuộc nhau) — Vì sao: Phải nối chứng từ rời, cộng DT 3 tháng theo ngành, chọn phương pháp, điền form, rồi nộp eTax; bước sau phụ thuộc số bước trước.

**Bài toán nhóm nằm ở ô nào:**

```text
Độ mơ hồ thấp × Độ phức tạp cao → Workflow điều phối nhiều bước rõ, chưa cần Agent.
```

**Vì sao (2-3 câu):**

```text
Đường đi cố định: chứng từ → tổng hợp → giải thích/điền nháp → người review → người nộp. AI không phải tự chọn tool hay đổi kế hoạch từng hộ. Phần đúng/sai nằm ở số liệu và chỉ tiêu, nên Rule giữ các bước có bảng; AI chỉ hỗ trợ đọc chứng từ và diễn giải field.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? (Dùng cho bước nào?) |
|---|---|---|---|---|
| **Rule** | Checklist chứng từ Điều kiện 01/CNKD; bảng tỷ lệ GTGT/TNCN theo ngành; ngưỡng 500 triệu; gợi ý PP1 nếu DT 500tr–3tỷ; template Excel cộng 3 tháng; hướng dẫn 15 bước eTax in sẵn | Đủ nếu hộ đã có tổng DT theo ngành và chỉ cần nhớ nộp gì. HTKK đã tính thuế khi số đã nhập | Không đọc hóa đơn rời; không giải thích field bằng tiếng bán hàng; <2% hộ Bắc Ninh có phần mềm nên phần lớn chưa có số sẵn | Dùng cho bước 2 (checklist) và bước 6 (lưu đối chiếu). Không đủ làm toàn bộ |
| **Workflow** | Rule checklist → AI gắn nhãn HĐ / cộng DT / giải thích chỉ tiêu / draft số lên form nháp → chủ hộ đối chiếu → chủ hộ tự nộp eTax | Đủ vì luồng tuyến tính, AI chỉ 1 cụm bước ngôn ngữ + đọc ảnh, người giữ nút nộp | AI gắn sai ngành, cộng sai DT, giải thích luật cũ (TT 18 vs TT 50). Cần flag “không chắc” | **Chọn** làm khung chính |
| **Agent** | Agent tự kéo HĐĐT từ nhà cung cấp, tự chọn PP, tự điền, tự nộp OTP/DVC | Chỉ cần nếu mỗi hộ có nhánh tool khác nhau và phải tự quyết bước tiếp theo khi thiếu giấy | Quyền truy cập thuế/HĐĐT, nộp sai không rollback, trách nhiệm pháp lý mơ hồ | Không chọn |

**5 câu hỏi chốt (trả lời câu đầy đủ):**
1. Rule có giải được 70-80% case không? Không, nếu case là hộ sổ tay. Rule giải tốt hộ đã có số tổng hợp (thiểu số). Với hộ chứng từ rời, checklist chỉ biết “thiếu/đủ giấy”, không biết điền ô nào.
2. Các bước có đi thẳng một đường không hay phải rẽ nhánh? Đi thẳng một đường cho scope PP1 / DT 500tr–3tỷ. Rẽ nhánh PP2, nhiều địa điểm, TMĐT không đưa vào v1.
3. Có thật sự cần Agent tự lập kế hoạch + gọi tool không? Không. Không cần tự gọi cổng thuế hay nhà cung cấp HĐĐT. Chủ hộ mang chứng từ vào, nhận nháp, tự nộp.
4. Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu? Chủ hộ đối chiếu với hóa đơn/sổ ở bước 4, mục tiêu phát hiện trong ~20 phút trước khi mở eTax. Chi cục phát hiện sau khi nộp thì đã muộn (trả hồ sơ / truy thu).
5. Có hạ được từ Agent → Workflow → Rule không? Có. Agent hạ về Workflow bằng cách cấm nộp thay. Workflow hạ về Rule (Excel + checklist + cầm tay chỉ việc) nếu AI sai số >70% draft trong 2 quý liên tiếp.

**Mức chọn:**

```text
Workflow (Rule cho checklist/ngưỡng; AI cho đọc chứng từ + giải thích field; người review và nộp).
```

**Vì sao chọn (3-4 câu):**

```text
Cổng nộp và HTKK đã giải bước format/tính thuế. Pain còn lại là đọc chứng từ rời và hiểu field — đúng chỗ ngôn ngữ/ảnh, không cần tự lập kế hoạch. Workflow khớp ma trận (phức tạp cao, mơ hồ thấp ở số liệu). Chủ hộ giữ boundary nên rủi ro pháp lý kiểm soát được hơn Agent. Research Phase 4 cũng chỉ ra pattern “sandbox + cầm tay chỉ việc”, không phải nộp thay.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

```text
Rule/Excel/đại lý đủ nếu hộ chịu nhập số hoặc trả 500K–1 triệu/quý. Phần lớn hộ sổ tay không qua được bước cộng DT theo ngành và không hiểu chỉ tiêu, đúng lúc TT 18 rồi TT 50 đổi mẫu. Rule một mình không kéo họ tới “sẵn sàng nhập eTax dưới 30 phút”.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

| Field | Nội dung |
|---|---|
| **Actor** | Chủ hộ vừa chuyển khoán → kê khai, DT ~500 triệu–3 tỷ/năm, tự làm tờ khai quý, chưa thuê đại lý, chưa dùng phần mềm bán hàng đầy đủ (tiệm tạp hóa, quán ăn, shop Facebook/TikTok). |
| **Workflow** | Gom chứng từ quý → cộng DT 3 tháng theo ngành → chọn PP1 và chỉ tiêu 01/CNKD → điền eTax/Cổng DVC → VNeID + OTP nộp → sửa nếu bị trả. Scope v1 chỉ PP1; chưa PP2, chưa nhiều địa điểm. |
| **Bottleneck** | Chọn phương pháp + điền chỉ tiêu khi không hiểu field (~60–90 phút lần đầu), cộng thêm cộng DT từ chứng từ rời (~75 phút). Cổng nộp không phải nút nghẽn. |
| **Impact** | Lần đầu ước lượng 3–5 giờ/quý; kê sai → trả hồ sơ, truy thu, phạt theo NĐ 310/2025; thuê đại lý ~500K–1 triệu/quý. Baseline giờ chưa bấm với chủ hộ thật. |
| **Success Metric** | (1) Từ lúc có chồng chứng từ đến sẵn sàng nhập eTax: ~2,5–3 giờ → dưới 30 phút. (2) Tổng lần đầu kể cả nộp: dưới 60 phút. (3) Trên bộ chứng từ pilot, số ô AI sai sau review không làm sai phương pháp/chỉ tiêu. Không đo bằng tờ khai nộp thật trong lab. |
| **Boundary** (làm / không làm) | Làm: checklist chứng từ, giải thích field, draft số từ chứng từ được cung cấp, gắn link TT 18/2026 hoặc TT 50/2026. Không làm: nộp tờ khai, ký OTP, bịa doanh thu, chọn PP khi thiếu căn cứ, tư vấn tối ưu thuế, kết nối API nhà cung cấp HĐĐT. |
| **AI intervention point** (can thiệp sau bước nào, trước bước nào) | Sau khi chủ hộ upload chứng từ và Rule báo checklist đủ/thiếu. Trước khi chủ hộ mở eTax để nhập và nộp. |
| **Mức chọn** (Rule / Workflow / Agent + 1 câu vì sao) | Workflow: đường đi cố định, AI một cụm bước, người giữ nút nộp — không cần Agent. |
| **Rủi ro & người thật kiểm tra** (rủi ro lớn nhất + ai kiểm tra bằng cách nào) | Rủi ro lớn nhất: AI cộng sai DT hoặc chọn sai ngành/PP, chủ hộ copy sang eTax. Người kiểm: chủ hộ đối chiếu từng dòng với hóa đơn/sổ; nếu AI gắn “không chắc” thì hỏi chi cục/đại lý, không nộp theo draft. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú (câu đầy đủ) |
|---|---|---|
| Actor + workflow rõ chưa? | Yes | Actor đã thu hẹp 500tr–3tỷ / quý / PP1; 7 bước hiện tại và 6 bước tương lai đã có input-output-thời gian. |
| Baseline + metric đo được chưa? | Not Yet | 3–5 giờ là ước lượng + blog 15 bước eTax, chưa bấm giờ với 1 chủ hộ. Metric lab chỉ đo trên bộ chứng từ mẫu. |
| Data/input đủ dùng chưa? | Not Yet | Chưa có quyền HĐĐT thật. Đủ cho pilot nếu có 1 quý hóa đơn mẫu (giấy/PDF) do nhóm tự chuẩn bị. |
| AI sai, hậu quả chấp nhận được không? | Not Yet nếu nộp thật / Yes nếu sandbox | Nộp theo số sai → phạt/truy thu, không chấp nhận. Draft trong sandbox, người nhập tay sau review thì chấp nhận được. |
| Có người review/owner không? | Yes | Chủ hộ là owner số liệu và nút nộp. Trong lab, thành viên nhóm đóng vai reviewer trên bộ mẫu. |
| Có cách non-AI đơn giản hơn không? | Yes, nhưng không phủ 100% pain | Checklist + HTKK + đại lý / cầm tay chỉ việc đã có. Chúng không giải thích field và không đọc chứng từ rời cho hộ chưa dùng phần mềm. |

**Decision:**

```text
Go với scope nhỏ (sandbox). Chưa Go production / chưa nộp hệ thống thuế thật.
```

**Lý do (3-4 câu dựa trên bằng chứng):**

```text
Actor, workflow, bottleneck và boundary đủ chặt để chạy pilot trong lab: AI chỉ draft, người nộp. Research cho thấy eTax/HTKK/MISA đã chiếm bước nộp và sổ sách, khoảng trống đúng là hiểu field + đối chiếu chứng từ. Baseline thời gian và hóa đơn thật chưa có nên không tuyên bố “giảm 4 giờ → 60 phút” trên hộ thật. Hậu quả AI sai khi nộp thật không chấp nhận được; sandbox + human review là mức Go nhỏ nhất còn an toàn.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

```text
Data: 1 bộ hóa đơn + sổ tay giả lập 1 quý của 1 tiệm tạp hóa (DT trong khoảng 500tr–3tỷ, 1 ngành).
Chạy tay: chủ hộ (hoặc thành viên đóng vai) chụp chứng từ → checklist Rule → prompt cố định để AI gắn nhãn/cộng DT/giải thích 5 chỉ tiêu → người sửa → người tự điền eTax (không nộp, hoặc nộp trên Cổng trải nghiệm nếu có).
Đo 3 số: (1) phút từ lúc có chứng từ đến lúc form nháp sẵn; (2) số ô AI sai so với cộng tay; (3) số lần AI phải gắn “không chắc” / người bỏ draft.
```

**Nếu Not Yet — cần validate gì trước:**

```text
Trước khi mở rộng khỏi sandbox: phỏng vấn 2–3 chủ hộ (bấm giờ lần kê gần nhất, bước đau nhất, có thuê đại lý không); xác nhận mẫu đang dùng là TT 18 hay TT 50 theo kỳ kê; thử 1 bộ chứng từ thật (che MST nếu cần).
```

**Nếu No-Go — làm gì thay AI:**

```text
Không chọn No-Go toàn bộ. Nếu pilot cho thấy AI sai số >70% ô, hạ về Rule: checklist + Excel + hướng dẫn eTax / đại lý thuế, không giữ lớp AI.
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

```text
Dừng AI trên bước số liệu nếu 2 quý liên tiếp (hoặc 2 bộ chứng từ pilot) người phải sửa >70% draft, hoặc AI bịa DT/PP không có trên chứng từ. Khi đó quay về Excel + checklist + HTKK/eTax. Dừng hẳn nếu phát hiện draft được copy nộp thật mà không review.
```

---

### Self-check nộp phần 02 (nhóm)
- [x] Có nhật ký hội tụ 9-12 → 1 (cluster + shortlist + score)
- [x] Có validation (poll 8 bạn + quote công khai; chưa interview chủ hộ tại cửa hàng) + research (link kiểm được)
- [x] Có workflow trước/sau đủ thời gian, handoff, bottleneck, boundary, fallback
- [x] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có làm/không làm
- [x] Có so sánh Rule/Workflow/Agent + Decision Go/Not Yet/No-Go có lý do
