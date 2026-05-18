---
artifact: 1 — Track & Big Ask + 2 — Tool Breakdown
bai-tap: Frame — nghe đúng đề rồi tách nhỏ
phase: Double Diamond vòng 1 · ◇ giãn (nghe rộng, chưa chốt)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 00-context.md · track card · prompts/01-breakdown.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 1 — Intake & Breakdown: nghe đúng đề, tách nhỏ

Mục tiêu: cả nhóm hiểu giống nhau "công cụ lớn stakeholder muốn", rồi tách nó thành 5–8 use case nhỏ làm được riêng. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1 — nghe rộng, tách rộng, chưa chọn.

Lý do làm bước này: hai cái bẫy chết người ở đây. Một, nhận đề literal ("làm con chatbot") rồi nhảy vào build — trong khi yêu cầu mơ hồ thường chỉ là triệu chứng. Hai, ôm cả công cụ lớn đi pitch "build cả platform" → trượt Gate 1 ngay. Tách nhỏ là động tác bắt buộc để từ "một ý tưởng to" sang "danh sách phần làm được".

Quy tắc: **nghe trước, tách trước, chưa chọn.** Bước này không được chốt Quick Win (việc đó ở file `2`).

## Bước 0 — Đọc track card + 00-context (2 phút)

Đọc track card được giao và `00-context.md` (mục 2 đã điền). Đừng lướt.

## Quy trình 12 phút

```text
2 phút  — Bước 0: đọc track card + context
4 phút  — Phần A: phát biểu lại Big Ask bằng lời nhóm
6 phút  — Phần B: tách 5–8 use case + check độc lập
```

---

## Phần A — Phát biểu lại Big Ask bằng lời nhóm

Đừng chép lại đề. Cả nhóm nói lại "công cụ lớn stakeholder muốn" bằng lời mình. Nếu 3 người nói 3 kiểu khác nhau → chưa hiểu giống nhau, bàn thêm.

Câu hỏi phụ (tự trả lời):

- Stakeholder nói họ muốn gì, và họ thực sự *cần* gì — có khác nhau không?
- "Tại sao bây giờ?" — ở quy mô ~500 người, cái gì đang đau khiến phải làm công cụ này lúc này?
- Ai là người dùng đầu tiên thật sự, không phải "cả khóa"?

### Trả lời

- **Big Ask, viết lại bằng lời nhóm (2–3 câu)**: Stakeholder muốn xây dựng một hệ thống AI tự động tạo câu hỏi trắc nghiệm và câu hỏi ngắn từ tài liệu bài học (slide, handbook), đồng thời tự động chấm điểm mang tính chất định hướng (formative). Hệ thống giúp học viên tự kiểm tra kiến thức, phát hiện ngay các lỗ hổng hoặc hiểu lầm (misconceptions) trước khi bước vào làm lab hoặc thuyết trình, đồng thời cung cấp cho giảng viên/coach góc nhìn tổng quan về các lỗi sai phổ biến của cả lớp.
- **Tại sao bây giờ**: Với quy mô ~500 học viên (và ~80 học viên riêng track Product), việc tạo quiz thủ công tốn rất nhiều thời gian của instructor, trong khi coach không thể chấm bài tập nhỏ hay giải thích lỗi sai cho từng người. Học viên thường mang nguyên các hiểu lầm (ví dụ: nhầm lẫn giữa AI Pilot Plan và Project Plan truyền thống, hoặc lạm dụng "tự build AI" thay vì Buy/Boost) vào thẳng buổi làm lab và buổi present, dẫn đến kết quả lab kém và mất thời gian sửa sai trên lớp.
- **Người dùng đầu tiên cụ thể**: ~80 học viên của track Product trong khóa AI20k (cụ thể ở bài học Day 28) và các Lab Coach phụ trách theo dõi tiến độ của họ.

## Phần B — Tách công cụ lớn thành 5–8 use case

Nhìn mục **Big Vision Modules** trong track card. Mỗi dòng = 1 use case làm được riêng, viết dạng *"AI làm X cho ai để họ Y"* — không phải tính năng mơ hồ. Cần 5–8 dòng (ít hơn 5 = chưa tách đủ; nhiều hơn 8 = đang liệt kê vụn).

| # | Use case (AI làm gì · cho ai · để họ làm được gì) | Người dùng | Làm được độc lập? |
|---|---|---|---|
| 1 | AI tự động sinh bộ quiz 10 câu (trắc nghiệm & câu hỏi ngắn) từ tài liệu Day 28 (skeleton + handbook) cho học viên để họ tự kiểm tra kiến thức trước giờ làm lab. | Học viên | Có |
| 2 | AI tự động chấm điểm formative cho các câu trả lời ngắn (vd: phân biệt AI Pilot Plan vs Project Plan) dựa trên rubric chuẩn để học viên biết lý do mình sai. | Học viên | Có |
| 3 | AI tổng hợp và phát hiện Top 3 hiểu lầm phổ biến (misconceptions - vd: hiểu sai về Build/Buy/Boost) từ bài làm của cả lớp cho instructor/coach để họ kịp thời giải thích lại trong buổi live. | Instructor, Coach | Không — phụ thuộc #1 và #2 |
| 4 | AI tự động sinh lộ trình học bù và gợi ý chính xác trang tài liệu/slide cần đọc lại cho từng học viên làm sai để họ tự khắc phục lỗ hổng kiến thức. | Học viên | Không — phụ thuộc #2 |
| 5 | AI tạo dashboard thống kê tỷ lệ làm đúng/sai theo từng concept (Frame, Solution, Pilot Plan) cho instructor để họ điều chỉnh trọng tâm bài giảng. | Instructor | Không — phụ thuộc #1 và #2 |
| 6 | AI tự động sinh quiz phân hóa theo 3 level (Cơ bản/Áp dụng/Nâng cao) cho học viên để họ thử thách bản thân theo năng lực riêng. | Học viên | Có |
| 7 | AI tạo cơ chế "Giải thích Socratic" (đặt câu hỏi gợi mở thay vì đưa đáp án thẳng) cho học viên khi họ làm sai quiz để họ tự suy nghĩ và hiểu sâu hơn. | Học viên | Không — phụ thuộc #2 |

Cần ít nhất **4 use case thật sự độc lập** (làm được mà không cần cái khác xong trước). Nếu nhiều cái phụ thuộc nhau → gộp hoặc viết lại cho tách bạch.

---

## Phát hiện ban đầu

- Việc sinh quiz trắc nghiệm (MCQ) rất dễ làm nhưng mang lại giá trị thực tế không cao bằng việc chấm câu trả lời ngắn (Short Answer), vì học viên AI20k thường hổng ở tư duy lập luận (như cách chọn Build/Buy/Boost) chứ không phải thuộc lòng khái niệm.
- Rào cản lớn nhất và rủi ro nhất là AI chấm sai câu trả lời mở hoặc nhận diện sai misconception, khiến học viên hoang mang hoặc khiếu nại. Do đó, hệ thống chỉ dừng ở mức "formative" (góp ý học tập) và cần có bộ rubric cực kỳ chi tiết kèm dẫn chứng tài liệu gốc.

## Câu hỏi mở (mang sang bước chọn Quick Win)

- Làm thế nào để đảm bảo AI chấm câu hỏi ngắn (Short Answer) đạt độ đồng thuận (calibration) cao với đánh giá của Coach thật?
- Nên chọn làm phần sinh quiz trắc nghiệm trước cho dễ, hay tập trung ngay vào luồng tạo quiz + chấm câu hỏi ngắn cho Day 28 để giải quyết đúng nỗi đau lớn nhất?

---

## Tổng kiểm tra trước khi sang `2-quick-win.md`

| Hạng mục | Xong? |
|---|---|
| Cả nhóm phát biểu lại Big Ask giống nhau, không cần nhìn card | [x] |
| Có 5–8 use case dạng "AI làm X cho ai để Y" | [x] |
| Có ≥4 use case thật sự độc lập | [x] |
| Nhóm KHÔNG còn ý định pitch "build cả platform" | [x] |

Sau bước này, mở `2-quick-win.md` — chấm điểm chọn 1 lát cắt làm trước.

*Liên quan: handbook §A1+§A2 · `prompts/01-breakdown.md` · `00-context.md`*
