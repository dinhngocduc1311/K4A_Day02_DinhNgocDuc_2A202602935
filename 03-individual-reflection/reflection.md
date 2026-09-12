# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Đinh Ngọc Đức
- Mã học viên: 2A202602935
- Nhóm: Biệt đội ánh sáng
- Candidate problem nhóm chọn: Tự kê khai thuế 01/CNKD hằng quý

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Viết 10 problems từ công việc thực tế của một AI Engineer, chỉ ra nỗi đau ở các khâu chuẩn bị dữ liệu và đánh giá model. | Nhóm có thêm góc nhìn về các bài toán kỹ thuật B2B để so sánh với các bài B2C khác. |
| Pitch Problem Card | Trình bày bài "Đánh giá và gắn nhãn lỗi output AI" (Card #1). Phân tích rõ bottleneck tốn 35 phút đọc mẫu. | Đưa bài toán này vào thẳng danh sách Shortlist (Top 3) để cả nhóm chấm điểm. |
| Challenge bài của bạn khác | Đặt câu hỏi cho bài toán thuế của Long: "Làm sao kiểm chứng được luật thuế đang dùng là mới nhất và AI không bịa luật?" | Giúp nhóm nhận ra rủi ro pháp lý và quyết định thu hẹp scope, thắt chặt Human Boundary. |
| Gom trùng / cluster | Đọc và phân loại 15 candidates thành 4 cụm dựa trên tính chất Workflow và Bottleneck thay vì chia theo ngành nghề. | Giúp nhóm nhìn ra bức tranh chung (VD cụm D: Quyết định có rủi ro pháp lý) để dễ chọn bài. |
| Chọn candidate problem | Ban đầu phản biện tiêu chí "Làm trong lab" của bài #10 vì lo ngại rủi ro pháp lý; sau khi nhóm chốt thu hẹp scope vào sandbox, tôi đồng thuận chấm 5/5 (tổng 35/35). | Giúp nhóm chọn được candidate có impact lớn nhất với sự đồng thuận tuyệt đối (35/35) thay vì chọn bài an toàn. |
| Validation / research | Ghi chép và tổng hợp nội dung poll 8 bạn trong lớp; rà soát thông tin từ các app eTax Mobile và MISA. | Xác định được khoảng trống AI cần làm là giải thích field thay vì làm tool nộp thuế thay. |
| Workflow nhóm | Rà soát chéo sơ đồ quy trình hiện tại (7 bước) và tương lai (6 bước) do bạn Long vẽ, góp ý làm rõ ranh giới giữa bước 2 (Rule) và bước 3 (AI). | Workflow trước/sau logic, sát với thực tế, tách biệt rõ ràng giữa Rule và AI. |
| Problem Statement | **(Vai trò chính: Writer)** Chấp bút viết toàn bộ bản v0 và v1; gọt giũa câu chữ, rút gọn các ý lan man thành các gạch đầu dòng sắc bén. | Bản PS cuối cùng cực kỳ gãy gọn, nêu rõ ràng metric, giới hạn boundary của AI và rủi ro. |
| Rule / Workflow / Agent | Viết lập luận trả lời 5 câu hỏi chốt để bảo vệ việc chọn mức Workflow thay vì Agent cho bài toán thuế. | Báo cáo có sức thuyết phục cao khi giải thích được vì sao không cần một Agent tự lập kế hoạch. |
| Decision | Trình bày lý do Go / Not Yet, đưa ra phương án Fallback chi tiết. | Khẳng định được tính khả thi khi giới hạn bài toán ở mức sandbox. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Với vai trò Writer, dấu ấn lớn nhất của tôi là sự mạch lạc, súc tích và chặt chẽ của bản Problem Statement v1 cũng như toàn bộ phần lập luận hạ giải pháp từ Agent xuống Workflow. Tôi đã chắt lọc từ các ý tưởng thô của nhóm thành những câu chữ bảo vệ quyết định (đặc biệt ở phần Human Boundary) cực kỳ sắc bén trong báo cáo cuối.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Gợi ý mở rộng các vấn đề thường gặp của AI Engineer. | Giúp rà soát lại toàn bộ quy trình làm việc để không bỏ sót pain point (như khâu setup môi trường). | Đề xuất các trợ lý AI "toàn năng" tự động hóa toàn bộ việc code hoặc review. | Bỏ qua các ý tưởng Agent viển vông, chỉ tập trung vào các vấn đề hẹp, có baseline đo được bằng phút. |
| Problem Card | Gợi ý cấu trúc viết Problem 1 câu cho gọn. | Tìm được cách diễn đạt ngắn gọn bao gồm đủ Actor, Trigger và Pain. | Không áp dụng được văn phong B2B của tôi. | Tự viết lại toàn bộ nội dung dựa trên trải nghiệm thực tế của bản thân. |
| Workflow | Không dùng vì cần thảo luận trực tiếp bám sát thực tế nhóm. | (Không dùng) | (Không dùng) | Tự tư duy và đóng góp logic cho sơ đồ của nhóm. |
| Research | Dùng perplexity/search để tìm hiểu nhanh các app kê khai thuế hiện có như eTax hay HTKK. | Gom thông tin các tool đang có mặt trên thị trường rất nhanh chóng. | Không phân biệt được rõ các nghị định/thông tư sẽ áp dụng cho năm 2026. | Tự search Google để tìm nguồn quy định chính thức và sửa lại thông tin trong bảng research. |
| Problem Statement | Yêu cầu AI đóng vai người chấm bài phản biện bản PS v0. | Chỉ ra được điểm yếu chí mạng: "Metric dựa trên ước lượng 3-5 giờ nhưng chưa có interview thật". | Đưa ra các giải pháp sửa chữa quá chung chung kiểu "đi khảo sát thêm". | Tự thêm phần ghi chú rõ ràng vào báo cáo rằng baseline này đang là giả định, và thu hẹp pilot vào việc giả lập (sandbox). |
| Rule / Workflow / Agent | Không dùng vì cần tư duy logic độc lập để bảo vệ quyết định. | (Không dùng) | (Không dùng) | Tự viết dựa trên framework 5 câu hỏi của khóa học. |
| Decision | Không dùng vì quyết định liên quan rủi ro pháp lý cần con người tự đánh giá. | (Không dùng) | (Không dùng) | Tự viết dựa trên logic an toàn (chỉ nộp nháp). |

> Nếu phase nào không dùng AI, ghi `Không dùng` và vì sao tự làm.

---

## 3. Reflection câu hỏi mở

Chọn 3-4 câu trong 6 câu dưới để viết thành đoạn 8-12 câu (không trả lời bullet 1 dòng):
- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first, đòi làm Agent cho ngầu không?
- Tôi có thay đổi ý kiến sau khi bị challenge không, vì sao đổi?
- Tôi đóng góp gì thật sự vào artifact cuối, phần nào có dấu tay của tôi?
- Điều khó nhất khi viết Problem Statement là gì, metric hay boundary?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

**Reflection:**

```text
Ban đầu, tôi rất tin tưởng vào bài toán "Đánh giá output AI" của mình vì đó là nỗi đau thực tế tôi gặp hàng tuần và nắm rất rõ quy trình. Tuy nhiên, khi nghe bạn Long pitch bài toán "Tự kê khai thuế 01/CNKD", tôi bị thuyết phục hoàn toàn bởi impact xã hội sâu rộng của nó so với vấn đề kỹ thuật hẹp của cá nhân tôi. Dù phải gác lại "đứa con tinh thần", tôi đã chủ động thay đổi ý kiến để đồng thuận chọn bài toán thuế vì lợi ích chung của cả nhóm. Trong quá trình thảo luận giải pháp, nhóm cũng từng có lúc bị cuốn vào tâm lý solution-first khi muốn dựng hẳn một AI Agent tự động kết nối cổng dịch vụ công để nộp thuế cho ngầu. Tuy nhiên, sau khi phân tích kỹ ma trận độ phức tạp và rủi ro pháp lý nếu AI làm sai, tôi cùng nhóm đã kịp thời phanh lại để chốt mức Workflow an toàn. Với vai trò Writer, đóng góp thực sự và dấu tay rõ nét nhất của tôi trong artifact cuối cùng nằm ở sự gãy gọn của bản Problem Statement v1 và phần lập luận sắc bén bảo vệ quyết định hạ từ Agent xuống Workflow. Điều khó nhất đối với tôi khi viết Problem Statement không phải là đo lường metric, mà là làm sao định nghĩa được "Human Boundary" thật rạch ròi để kiểm soát rủi ro pháp lý. Tôi đã phải trau chuốt từng câu chữ để khóa chặt ranh giới: AI chỉ dừng ở mức giải thích chỉ tiêu và draft số liệu, còn quyền quyết định và nút bấm nộp tờ khai hoàn toàn thuộc về chủ hộ. Nếu được làm lại bước Validation, tôi chắc chắn sẽ challenge nhóm quyết liệt hơn ở khâu thu thập dữ liệu thực tế. Thay vì chỉ dừng lại ở micro poll 8 bạn trong lớp, tôi sẽ yêu cầu nhóm đi phỏng vấn và bấm giờ trực tiếp trên ít nhất một chủ hộ kinh doanh thật sự để baseline thời gian có bằng chứng đanh thép hơn.
```

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] [15đ] Nhóm có workflow trước/sau
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI
