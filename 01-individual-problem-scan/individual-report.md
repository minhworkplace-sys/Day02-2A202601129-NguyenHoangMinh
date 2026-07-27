
# Phase 1 — Individual Scan: tìm 5+ problems
## Bảng scan

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 |Lặp lại|PM phải viết PRD/User Story cho mỗi feature mới|Product Manager|Mỗi sprint đều dành vài giờ để viết tài liệu với cấu trúc gần như giống nhau|
| 2 |Lặp lại|Team họp xong phải tổng hợp Meeting Minutes và Action Items|PM, Scrum Master|Sau mỗi cuộc họp đều phải ghi chép và gửi lại biên bản qua Slack/Email.|
| 3 |Tốn thời gian|Tổng hợp báo cáo tiến độ dự án |PM|Cuối tuần phải lấy dữ liệu từ Jira, Git và nhiều nguồn khác để làm báo cáo.|
| 4 |Tốn thời gian|Đánh giá tác động khi khách hàng đổi requirement|PM, Tech Lead|Phải họp nhiều người để xác định module nào bị ảnh hưởng và estimate lại.|
| 5 |AI có thể hỗ trợ tốt hơn|Trả lời câu hỏi về tài liệu dự án|Developer, QA| Cùng một câu hỏi được hỏi nhiều lần mặc dù đã có tài liệu. |
| 6 |AI có thể hỗ trợ tốt hơn|Sinh User Story, Acceptance Criteria, Test Case |PM,QA |Nội dung chủ yếu theo mẫu, chỉ thay đổi theo từng feature. |
| 7 |AI có thể hỗ trợ tốt hơn|Tóm tắt cuộc họp và tạo Action Items|Cả Team |Mọi người không nhớ đầy đủ các quyết định hoặc việc cần làm sau cuộc họp.|
| 8 |Khó khăn đến từ người khác|Thành viên cập nhật Jira không đầy đủ hoặc không đúng trạng thái|PM |Jira hiển thị "In Progress" nhưng thực tế task đã hoàn thành hoặc đang bị block. |
| 9 |Khó khăn đến từ người khác|Khách hàng thay đổi requirement nhiều lần|PM, Developer |Feature phải sửa nhiều lần, estimate liên tục thay đổi. |
| 10 |Khó khăn đến từ người khác|Khách hàng báo bug nhưng mô tả không đầy đủ|QA, Developer|Bug report chỉ ghi "không chạy" hoặc "bị lỗi", thiếu bước tái hiện (Steps to Reproduce), log hoặc ảnh chụp màn hình nên mất nhiều thời gian xác minh. |

# Phase 2 — Top 3 Problem Cards + Draft Workflow

> Dữ liệu ở phần này được lấy từ Phase 1, dựa trên các problem đã scan từ trải nghiệm thực và các dấu hiệu thật trong worksheet.

## 1. Chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tổng hợp báo cáo tiến độ dự án từ nhiều nguồn | Workflow rõ, lặp lại mỗi tuần, có thể đo thời gian và tác động, AI có thể hỗ trợ phần viết narrative | Cần xác nhận phần nào là bottleneck thật sự và metric nên đo bằng thời gian hay số lần phải sửa |
| 2 | Tóm tắt cuộc họp và tạo Action Items | Có nhiều người bị ảnh hưởng, lặp lại sau mỗi cuộc họp, AI phù hợp để tóm tắt và cấu trúc việc cần làm | Cần chắc phần tóm tắt không bị quá phụ thuộc vào context của người tham dự |
| 3 | Sinh User Story, Acceptance Criteria và Test Case từ feature mô tả | Có mẫu chuẩn, lặp lại nhiều, AI có thể giúp draft nhanh | Cần kiểm tra chất lượng đầu ra có đủ độ chính xác cho QA và PM hay không |

---

## Problem Card #1 — Tổng hợp báo cáo tiến độ dự án

**Problem 1 câu:**
Mỗi tuần, PM mất nhiều thời gian để tổng hợp dữ liệu từ Jira, Sheets và Slack thành một báo cáo tiến độ có thể gửi cho leadership.

**Actor:**
Junior PM / PM chịu trách nhiệm viết báo cáo tiến độ cho team và quản lý.

**Thời điểm / bối cảnh:**
Cuối mỗi tuần, trước buổi sync với Engineering Manager và leadership.

**Current workflow 3-7 bước:**
1. Export dữ liệu từ Jira
2. Lấy số liệu từ Google Sheets
3. Đọc recap từ Slack
4. Tổng hợp thông tin vào file báo cáo
5. Viết phần narrative / insight
6. Review và format trước khi gửi

**Bottleneck:**
Bước viết narrative từ dữ liệu rời rạc là phần tốn thời gian nhất và dễ bị “blank page”.

**Impact:**
Mỗi tuần mất khoảng 60-90 phút cho một người; nếu chậm thì leadership nhận báo cáo muộn và thiếu context trước buổi họp.

**Success metric:**
Giảm thời gian tổng hợp từ khoảng 90 phút xuống dưới 30 phút; giảm số lần PM phải chỉnh sửa nhiều lần trước khi gửi.

**Non-AI alternative:**
Template báo cáo + dashboard chuẩn + checklist có thể giúp giảm khâu format, nhưng chưa giải quyết tốt phần viết insight và tóm tắt.

**AI hypothesis:**
AI có thể giúp cấu trúc dữ liệu và draft narrative ban đầu, rồi PM review và chỉnh sửa trước khi gửi.

**Quick gut:**
[ ] No AI / process fix
[x] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — 90 phút

[Export Jira: 10']
→ [Lấy metrics từ Sheets: 10']
→ [Đọc Slack recap: 15']
→ [Tổng hợp vào Docs: 15']
→ [Viết narrative: 25']  <-- bottleneck
→ [Review + format: 10']
→ [Gửi: 5']
```

### Draft future workflow

```text
FUTURE STATE — 25 phút

[Auto-pull data: 2']
→ [AI cấu trúc dữ liệu: 2']
→ [AI draft narrative: 3']
→ [PM review + edit: 15']  <-- human boundary
→ [PM gửi: 3']
```

---

## Problem Card #2 — Tóm tắt cuộc họp và tạo Action Items

**Problem 1 câu:**
Sau mỗi cuộc họp, team mất thời gian để ghi lại quyết định, tóm tắt nội dung và chuyển thành action items rõ ràng.

**Actor:**
PM / Scrum Master / người dẫn cuộc họp.

**Thời điểm / bối cảnh:**
Sau mỗi cuộc họp nội bộ hoặc cross-team.

**Current workflow 3-7 bước:**
1. Ghi chép cuộc họp trong lúc họp
2. Tổng hợp ý chính sau họp
3. Chuyển thành meeting notes
4. Viết action items và người phụ trách
5. Gửi cho team qua Slack hoặc email

**Bottleneck:**
Việc chuyển raw notes thành summary chuẩn và action items rõ ràng rất mất thời gian, nhất là khi nhiều người nói cùng lúc.

**Impact:**
Mỗi buổi họp có thể tốn 20-30 phút để tổng hợp lại; nếu bỏ sót action items thì team dễ hiểu sai hoặc quên việc cần làm.

**Success metric:**
Giảm thời gian tổng hợp sau họp từ 30 phút xuống còn dưới 10 phút; tăng tỷ lệ action items được ghi đầy đủ và đúng người chịu trách nhiệm.

**Non-AI alternative:**
Template meeting notes + checklist + người ghi chép riêng có thể cải thiện cấu trúc, nhưng vẫn cần người thật tổng hợp lại.

**AI hypothesis:**
AI có thể tạo bản tóm tắt đầu tiên và đề xuất action items từ đoạn hội thoại hoặc ghi chú.

**Quick gut:**
[ ] No AI / process fix
[x] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — 30 phút

[Ghi chép cuộc họp: 10']
→ [Tổng hợp ý chính: 10']
→ [Viết action items: 5']
→ [Gửi cho team: 5']
```

### Draft future workflow

```text
FUTURE STATE — 10 phút

[AI tóm tắt cuộc họp: 2']
→ [AI đề xuất action items: 2']
→ [Người dẫn cuộc họp review: 4']
→ [Gửi cho team: 2']
```

---

## Problem Card #3 — Sinh User Story, Acceptance Criteria và Test Case

**Problem 1 câu:**
Khi có một feature mới, PM và QA mất thời gian để chuyển yêu cầu thành User Story, Acceptance Criteria và Test Case theo mẫu chuẩn.

**Actor:**
PM / QA / Product Owner.

**Thời điểm / bối cảnh:**
Khi bắt đầu một feature mới hoặc khi requirement thay đổi.

**Current workflow 3-7 bước:**
1. Đọc requirement hoặc ticket
2. Xác định scope và user value
3. Viết User Story
4. Viết Acceptance Criteria
5. Viết Test Case
6. Review lại với team

**Bottleneck:**
Phần viết lại theo mẫu là lặp lại và có thể làm thủ công nhiều lần, khiến người làm mất thời gian cho việc cấu trúc thay vì suy nghĩ về nội dung thật.

**Impact:**
Mỗi feature có thể tốn 20-40 phút để viết lại các tài liệu này; nếu viết sơ sài thì QA và dev dễ hiểu sai requirement.

**Success metric:**
Giảm thời gian tạo tài liệu từ 40 phút xuống dưới 15 phút; giảm số lỗi hiểu requirement trong giai đoạn đầu.

**Non-AI alternative:**
Template mẫu và checklist có thể giúp chuẩn hóa, nhưng vẫn cần người viết nội dung từ đầu.

**AI hypothesis:**
AI có thể tạo draft đầu tiên dựa trên một prompt chuẩn và requirement ngắn.

**Quick gut:**
[ ] No AI / process fix
[x] Rule
[x] Workflow
[ ] Agent
[ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — 40 phút

[Đọc requirement: 10']
→ [Xác định scope: 10']
→ [Viết User Story: 10']
→ [Viết Acceptance Criteria + Test Case: 10']
```

### Draft future workflow

```text
FUTURE STATE — 15 phút

[AI draft mẫu từ requirement: 5']
→ [PM/QA review và chỉnh sửa: 8']
→ [Đóng gói thành tài liệu chuẩn: 2']
```

---

## 2. Card tôi muốn pitch nhất

**Card tôi muốn pitch nhất:**
Tổng hợp báo cáo tiến độ dự án.

**Vì sao:**
Vì đây là problem có workflow rõ, impact vừa đủ lớn, metric có thể đo bằng thời gian và có thể vẽ before/after workflow rất dễ dàng.

**Câu hỏi tôi muốn nhóm challenge:**
Liệu pain thật có nằm ở việc “viết narrative” hay ở việc “thu thập dữ liệu” từ nhiều nguồn? Nếu phần thu thập dữ liệu đã được chuẩn hóa bằng dashboard thì AI có còn cần thiết ở bước narrative không?
