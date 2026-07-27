# Reflection cá nhân — Day 02 Lab

## 1. Tôi đã tham gia những phần nào?

Trong lab này, tôi tham gia khá đầy đủ các phần từ đầu đến cuối của quy trình problem-first:

- Scan cá nhân: tôi góp phần tìm và phân loại các candidate problem từ trải nghiệm thực, đặc biệt là các vấn đề liên quan đến tổng hợp thông tin, quản lý task và báo cáo từ nhiều nguồn.
- Pitch: tôi trình bày được một số candidate problem cho nhóm, trong đó có vấn đề về tổng hợp báo cáo tiến độ từ nhiều nguồn.
- Phản biện: tôi đặt câu hỏi để kiểm tra xem problem có thật sự có bottleneck rõ, metric đo được và có phù hợp để dùng AI hay không.
- Research: tôi hỗ trợ nhóm nhìn vào các hướng giải pháp đã có sẵn và tránh việc tự suy nghĩ trong chân không.
- Workflow: tôi góp phần vẽ workflow trước/sau để thấy rõ bước nào là bottleneck, phần nào nên dùng rule, workflow hay AI.
- Problem Statement: tôi tham gia chỉnh lại cách diễn đạt problem sao cho rõ actor, workflow, bottleneck, impact và boundary.
- Decision: tôi cùng nhóm đánh giá lựa chọn nên đi theo hướng Workflow thay vì Agent, vì đây là mức phù hợp hơn với bài toán và rủi ro kiểm soát được.

Qua phần này, tôi nhận ra rằng vai trò của mình không chỉ là đưa ra ý tưởng, mà còn là người giúp nhóm giữ đúng tư duy problem-first và không chạy theo solution-first.

---

## 2. Bảng dùng AI

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI còn hạn chế / sơ sài ở đâu? | Tôi đã điều chỉnh thế nào? |
|---|---|---|---|---|
| Scan cá nhân | Gợi ý thêm vấn đề từ nhiều góc nhìn khác nhau | Giúp mở rộng danh sách candidate và nhìn thấy các vấn đề lặp lại trong đời sống học tập và công việc | Một số ý tưởng bị quá rộng hoặc không có workflow thật, nên dễ bị kéo sang solution-first | Tôi chỉ giữ lại những vấn đề có actor rõ, workflow có thể vẽ và bottleneck cụ thể |
| Pitch / phản biện | Nhờ AI gợi ý câu hỏi để challenge bản thân và nhóm | Giúp mình nhìn ra điểm còn mơ hồ trong problem card như metric, scope và boundary | AI có thể đề xuất giải pháp quá sớm hoặc làm mình tin vào một ý tưởng chưa đủ bằng chứng | Tôi không dùng AI để quyết định thay mình; chỉ dùng để hỏi ngược và kiểm tra lập luận |
| Research | Tìm các ví dụ và công cụ tương tự để biết pattern đã có sẵn | Giúp nhóm hiểu rằng nhiều hệ thống đã dùng AI ở một bước cụ thể, không nhất thiết phải “build agent toàn năng” | Một số nguồn không có dữ liệu cụ thể về hiệu quả thật, nên không thể dùng làm bằng chứng tuyệt đối | Tôi chỉ giữ các nguồn có tính tham khảo và dùng chúng để hỗ trợ lập luận, không copy số liệu một cách mù quáng |
| Workflow | Hỗ trợ trình bày workflow trước/sau rõ hơn | Rất hữu ích để hình dung bottleneck và chỗ nào AI nên can thiệp | AI có thể gộp các bước lại khiến bottleneck bị che khuất | Tôi tự tách lại từng bước và xác định điểm nào là human boundary |
| Problem Statement | Nhờ AI phản biện về cách viết sao cho đủ actor, workflow, impact và metric | Giúp mình thấy được đâu là phần còn mơ hồ | AI có thể làm cho câu viết nghe “rất tốt” nhưng chưa thật sự chặt về scope | Tôi tự chỉnh lại để đảm bảo problem không quá rộng và có boundary rõ |
| Decision | Hỗ trợ suy nghĩ về Rule / Workflow / Agent và lựa chọn mức phù hợp | Giúp mình nhìn rõ vì sao Workflow hợp lý hơn Agent trong tình huống này | AI không thể thay thế quyết định của nhóm vì quyết định còn phụ thuộc vào bối cảnh và rủi ro | Nhóm tự chốt quyết định dựa trên bằng chứng, workflow và mức độ rủi ro |

---

## 3. Câu hỏi mở trong worksheet

### Học được gì?

Tôi học được rằng một bài toán tốt không phải là bài toán “có AI” mà là bài toán có người gặp vấn đề rõ, workflow rõ, bottleneck rõ và metric đo được. Nếu không có những yếu tố đó, AI dù có mạnh đến đâu cũng dễ trở thành giải pháp quá rộng và không hiệu quả.

Tôi cũng hiểu rõ hơn rằng việc vẽ workflow trước khi chọn AI là rất quan trọng. Workflow giúp thấy được đâu là phần nên dùng Rule, đâu là phần nên dùng Workflow, và đâu là phần không nên tự động hóa vì có rủi ro cao.

### Lúc nào nhóm đi theo hướng solution-first?

Nhóm có nguy cơ đi theo hướng solution-first khi bắt đầu từ một công cụ hoặc một ý tưởng AI mà chưa thật sự hiểu rõ bài toán. Trong lab này, điều đó xảy ra khi có một số candidate quá rộng hoặc nhìn chung chung như “tổng hợp thông tin”, “quản lý thông báo” mà chưa nói rõ actor và bottleneck cụ thể. Khi nhóm nhận ra điều này, chúng tôi dừng lại và quay về việc làm rõ workflow và impact trước.

### Nếu làm lại, mình sẽ đổi gì?

Nếu làm lại, tôi sẽ:
- chọn problem từ sớm hơn với scope rõ và metric cụ thể hơn,
- challenge nhiều hơn về “pain thật” trước khi quyết định chọn candidate,
- dùng AI nhiều hơn ở bước phản biện và kiểm tra logic, nhưng ít hơn ở bước quyết định,
- chuẩn bị workflow và metric sớm hơn để tránh bị kéo vào giải pháp quá sớm.

Tổng thể, lab này giúp tôi hiểu sâu hơn về cách làm việc với AI: không phải “đưa bài toán cho AI”, mà là “đưa bài toán vào đúng khung tư duy để AI có thể hỗ trợ đúng chỗ”.