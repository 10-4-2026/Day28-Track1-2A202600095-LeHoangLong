---
artifact: 3 — Quick Win Selection
bai-tap: Frame — chọn lát cắt làm trước
phase: Double Diamond vòng 1 · ◆ siết (hội tụ về 1 lựa chọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-intake-breakdown.md · prompts/02-quick-win-challenge.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 2 — Quick Win: chọn lát cắt làm trước

Mục tiêu: từ 5–8 use case ở file `1`, chấm điểm nhanh và chốt **1 Quick Win** để pilot đầu tiên — kèm lý do chọn và lý do *không* chọn các phần khác. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1.

Lý do làm bước này: đây là quyết định quan trọng nhất của phase Frame. Quick Win **không phải** phần dễ nhất hay nghe hay nhất — là phần *chứng minh được giá trị nhanh và có người ủng hộ*. Chọn sai → pilot fail → mất uy tín → khó xin pilot tiếp. Nhóm phải chọn được *và bảo vệ được bằng lý do*, không bằng cảm tính.

Quy tắc: **điểm số chỉ là gợi ý, không phải đáp án.** Đừng để con số quyết thay nhóm — nó chỉ giúp so sánh.

## Bước 0 — Lấy 4–6 use case mạnh nhất từ file `1` (1 phút)

## Quy trình 10 phút

```text
1 phút  — Bước 0: chọn 4–6 ứng viên
5 phút  — Phần A: chấm điểm 4 trục
3 phút  — Phần B: 1 lý do nên / 1 lý do không cho top 2
1 phút  — Phần C: chốt + ai ủng hộ + cái KHÔNG chọn
```

---

## Phần A — Chấm điểm 4 trục (1–5 mỗi trục)

Câu hỏi phụ (tự trả lời):

- "Risk" ở đây là *sai thì mất gì* — chọn đúng việc chính của user (task centrality) thì sai cũng đỡ đau; chọn việc lớn nhất thì sai rất đắt. Use case nào risk thấp thật?
- Use case nào có sẵn data + có người trong AI20k thật sự muốn dùng?

| Use case | Impact | Feasibility | Evidence nhanh | Risk (cao = an toàn) | Tổng |
|---|:--:|:--:|:--:|:--:|:--:|
| UC1: Sinh quiz 10 câu (MCQ + Short Answer) từ tài liệu D28 | 4 | 5 | 5 | 4 | 18 |
| UC2: Chấm formative câu trả lời ngắn (vd: Pilot Plan vs Project Plan, Build/Buy/Boost) | 5 | 4 | 4 | 3 | 16 |
| UC3: Tổng hợp Top 3 misconceptions (hiểu sai Build/Buy/Boost) & gợi ý học lại | 5 | 4 | 4 | 4 | 17 |
| UC6: Sinh quiz phân hóa 3 level (Cơ bản/Áp dụng/Nâng cao) | 3 | 3 | 3 | 4 | 13 |
| Combo Quick Win (UC1 + UC2 + UC3 cho riêng Day 28): Tạo quiz D28, chấm Short Answer & phát hiện misconception Build/Buy/Boost | 5 | 4 | 5 | 4 | 18 |

*(Ghi chú: Nhóm chọn đóng gói UC1, UC2 và UC3 thành một luồng Quick Win hoàn chỉnh cho riêng Day 28, vì nếu chỉ tạo quiz mà không chấm câu hỏi ngắn và không chỉ ra hiểu lầm thì không giải quyết được trọn vẹn pain point của học viên).*

## Phần B — 1 lý do nên / 1 lý do không, cho top 2

**Ứng viên A — Combo Quick Win D28 (Tạo quiz 10 câu D28, chấm Short Answer & phát hiện misconception Build/Buy/Boost kèm gợi ý học lại)**

```text
Nên chọn vì: Giải quyết trực tiếp điểm nghẽn lớn nhất của Day 28 (học viên không hiểu rõ bản chất Build/Buy/Boost và sự khác biệt của AI Pilot Plan trước giờ làm lab). Mang lại giá trị "end-to-end" tức thì, chứng minh được hiệu quả ngay trong 1 tuần pilot với track Product (~80 học viên).
Không nên vì: Đòi hỏi phải xây dựng prompt và rubric chấm Short Answer rất chặt chẽ để tránh AI chấm sai hoặc nhận diện sai misconception.
```

**Ứng viên B — UC1: Chỉ sinh bộ quiz trắc nghiệm (MCQ) tự động từ tài liệu Day 28**

```text
Nên chọn vì: Cực kỳ dễ làm (Feasibility 5/5), rủi ro kỹ thuật gần như bằng 0, có thể triển khai ngay lập tức bằng các công cụ AI cơ bản.
Không nên vì: Impact thấp. Trắc nghiệm chỉ kiểm tra khả năng ghi nhớ bề mặt, không giúp phát hiện các lỗ hổng tư duy sâu (như sai lầm trong lập luận chọn Quick Win hay Build/Buy/Boost), dễ dẫn đến tình trạng học viên "học mẹo" để qua bài.
```

## Phần C — Chốt Quick Win

- **Quick Win nhóm chọn**: Hệ thống Quiz & Auto Grading D28 (Tạo quiz 10 câu từ handbook Day 28, tự động chấm formative câu trả lời ngắn, phát hiện misconception về Build/Buy/Boost và gợi ý tài liệu học lại).
- **Vì sao chọn cái này trước** (2–4 câu, bám điểm + impact + evidence nhanh): Lát cắt này tập trung vào đúng 1 bài học (Day 28) và 1 nhóm đối tượng (~80 học viên track Product), giúp thu hẹp phạm vi triển khai nhưng tạo ra tác động lớn nhất. Việc chấm câu hỏi ngắn và phát hiện misconception giúp học viên nhận ra lỗ hổng tư duy ngay lập tức trước khi vào làm lab, tiết kiệm hàng chục giờ sửa bài của coach và nâng cao chất lượng artifact cuối cùng.
- **Ai trong AI20k sẽ ủng hộ pilot này** (và vì sao họ care — "có người ủng hộ" thường quan trọng hơn "impact cao"): Head of Academic / Lead Instructor (vì giúp đảm bảo chất lượng đầu ra của học viên trước khi bước vào 6 tuần thực tập tại doanh nghiệp mà không làm tăng tải cho đội ngũ giảng viên) và các Lab Coach (vì giảm tải việc phải giải thích đi giải thích lại các lỗi sai căn bản về Build/Buy/Boost cho từng nhóm).
- **Nhóm KHÔNG chọn gì + vì sao** (≥2 use case bị loại): 1. Không chọn UC5 (Xây dựng Dashboard thống kê toàn diện cho cả khóa học): Vì tốn kém chi phí tích hợp sâu vào LMS/phần mềm hiện tại, thời gian phát triển lâu, không mang lại giá trị trực tiếp cho học viên trong ngắn hạn.  2. Không chọn UC6 (Sinh quiz phân hóa 3 level phức tạp cho toàn bộ 30 ngày học): Quy mô quá lớn, rủi ro phình to scope (scope creep), chưa kiểm chứng được chất lượng chấm tự động trên 1 bài cụ thể thì việc mở rộng ra toàn khóa là mạo hiểm và lãng phí budget.

---

## Phát hiện ban đầu

- Khách hàng thực sự mua "sự cải thiện kiến thức" (thông qua phát hiện misconception và gợi ý học lại) chứ không mua "công cụ tạo câu hỏi". Do đó, tính năng Auto Grading + Misconception Detection mới là "core value" của Quick Win này.

## Câu hỏi mở (mang sang Problem Framing)

- Baseline hiện tại của việc học viên hiểu sai kiến thức Day 28 trước khi làm lab là bao nhiêu? (Cần ước lượng bằng số liệu thực tế từ các khóa trước).
- Cần đặt ngưỡng chính xác (accuracy/calibration rate) giữa AI và Coach là bao nhiêu phần trăm để hệ thống được phép chính thức áp dụng cho học viên?

---

## Tổng kiểm tra trước khi sang `3-FINAL-problem-framing.md`

| Hạng mục | Xong? |
|---|---|
| Có bảng chấm 4 trục cho ≥4 use case | [x] |
| Chốt 1 Quick Win, lý do bám số/impact (không "nghe hay") | [x] |
| Nêu rõ ai ủng hộ pilot này | [x] |
| Ghi rõ ≥2 phần KHÔNG chọn + lý do | [x] |

⚑ Đây là phần coach kiểm tra ở Mốc 1: *"Vì sao không làm full tool? Vì sao chọn lát cắt này trước?"*

Sau bước này, mở `3-FINAL-problem-framing.md` — đóng khung vấn đề thật (bản nộp của phase Frame).

*Liên quan: handbook §A3 · `templates/quick-win-scoring.md` · `prompts/02-quick-win-challenge.md`*
