---
artifact: 7 — AI Pilot Plan core
bai-tap: Pilot Plan — cam kết hai chiều: xin – hứa – đo – dừng
phase: Double Diamond vòng 2 · ◇ giãn → ◆ siết (liệt kê hết rồi chốt gọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 02-solution/2-FINAL-solution.md · 00-context.md · prompts/06-pilot-plan-challenge.md
nop-cuoi: Không — file trung gian (bản nộp ở 2-FINAL-pitch.md)
---

# 1 — AI Pilot Plan core

Mục tiêu: viết phần kế hoạch xin pilot — scope, người, data, budget, timeline, metric, exit criteria, adoption, lời hứa, lời xin. Bước này giãn ra (liệt kê hết những thứ cần) rồi siết lại (chốt bản gọn đủ để stakeholder quyết).

Lý do làm bước này: đây là thứ stakeholder dùng để **quyết approve hay dừng**. AI Pilot Plan **không phải proposal xin tiền** — là *cam kết hai chiều*: nhóm xin nguồn lực, đổi lại hứa giao evidence + chấp nhận dừng nếu metric fail. Demo đẹp mà không nói được "xin gì, hứa gì, đo gì, dừng khi nào" → trượt Gate 5.

Quy tắc: **budget tách từng hạng mục, không gộp 1 cục; không có mục "miscellaneous".** Exit criteria phải có người có quyền thực thi, không chỉ trên giấy.

## Quy trình 10 phút

```text
6 phút  — Điền 10 mục core (kéo nguyên liệu từ 00 + 01-frame + 02-solution)
3 phút  — Phần exit criteria + adoption (chỗ nhóm hay bỏ quên)
1 phút  — Tự phản biện
```

---

## 10 mục core

Câu hỏi phụ (tự trả lời):

- Nếu tóm vấn đề không gọn trong 1 câu → nhóm chưa hiểu vấn đề.
- Exit criteria của nhóm có ai DÁM thực thi khi sếp vẫn thích pilot không?
- Adoption: ai dùng đầu tiên — không phải "cả khóa ~500 người"?

### Trả lời

1. **Tóm vấn đề** (1 câu, từ Problem Framing): Trước giờ làm Lab Day 28, ~80 học viên track Product thiếu công cụ kiểm tra kiến thức thực chiến, dẫn đến việc họ mang các hiểu lầm căn bản về Build/Buy/Boost vào buổi lab, làm lãng phí ~1 giờ công giải thích của đội ngũ Coach và khiến 40% bài nộp bị trượt Gate 4.
2. **Cách làm + lý do** (từ 02-solution, 1 câu): Sử dụng chiến lược Boost (tích hợp API Gemini 1.5 Pro kết hợp RAG tài liệu D28 và Few-shot Prompting qua giao diện Web/Discord bot) vì đây là giải pháp tối ưu nhất về chi phí (~$25), tốc độ triển khai nhanh và cho phép kiểm soát hoàn toàn tri thức đặc thù của khóa học.
3. **Scope pilot**:
   - *Đối tượng phục vụ*: ~80 học viên thuộc track Product và 3 Lab Coach phụ trách.
   - *Thời gian*: Triển khai thử nghiệm trong 1 tuần (tập trung trọn vẹn vào nội dung Day 28 trước khi học viên bước vào giai đoạn 6 tuần thực chiến).
   - *Giai đoạn (Phases)*:
     + Phase 1 (3 ngày đầu): Internal testing & Calibration (Thử nghiệm nội bộ giữa AI và Coach trên 30 bài mẫu).
     + Phase 2 (4 ngày tiếp theo): Mở rộng cho 80 học viên track Product sử dụng trước giờ làm Lab D28.
4. **Người**:
   - *Nhóm thực thi*: Nhóm G08 (Trịnh Uyên Chi - PM/Prompting, Lê Hoàng Long - RAG/Backend, Nguyễn Phạm Trà My - QA/Metrics).
   - *Người review output rủi ro cao*: 3 Lab Coach (xử lý các ca học viên bấm nút khiếu nại).
   - *Người có quyền quyết approve/dừng*: Program Lead (Sponsor) và Lead Instructor.
5. **Data**:
   - *Dữ liệu sử dụng*: Handbook & Slide Day 28 chuẩn, Rubric chấm Short Answer, danh sách Top 5 Misconceptions (đặc biệt về Build/Buy/Boost) và 30 câu trả lời mẫu từ các khóa trước.
   - *Cơ chế bảo mật & trích dẫn*: Toàn bộ dữ liệu truyền qua API thương mại có cam kết bảo mật (không dùng để train model). Hệ thống bắt buộc trích dẫn chính xác số trang/mục trong handbook D28 cho mọi lời giải thích.
6. **Budget** (tách hạng mục):
   - *LLM API (Gemini 1.5 Pro / GPT-4o)*: $15 (dự phòng cho ~500 lượt chấm và test nghiệm thu).
   - *Hosting / Serverless (Vercel / Streamlit / Discord bot)*: $10 (chi phí duy trì server và database log nhỏ trong 1 tháng).
   - *Thời gian người (Human cost - Hạng mục ẩn)*: 15 giờ công của nhóm G08 để thiết lập hệ thống + 3 giờ công của Lead Instructor để duyệt prompt/rubric + 5 giờ công tổng hợp của các Coach để tham gia calibration.
   - *Tổng ngân sách tiền mặt xin cấp*: **$25**.
7. **Timeline + cổng giữa phase**:
   - *Ngày 1 - 2*: Thiết lập Knowledge Base (RAG), viết Prompt và xây dựng giao diện Discord bot/Web app.
   - *Ngày 3 (Cổng kiểm duyệt - Gate 1)*: Chạy Benchmark trên 30 bài mẫu. Lead Instructor nghiệm thu. *Điều kiện qua cổng*: Calibration rate ≥85%, Hallucination = 0%.
   - *Ngày 4 - 6*: Rollout cho 80 học viên track Product vào làm Quiz trước giờ lab. Theo dõi hệ thống real-time.
   - *Ngày 7 (Cổng tổng kết - Gate 2)*: Tổng hợp báo cáo Top 3 misconceptions của lớp gửi Instructor trước buổi học live, đánh giá adoption và chốt phương án mở rộng.
8. **Metrics** (SMART + baseline + ngưỡng + ai đo):

| Metric | Đo bằng gì · ai đo | Baseline | Ngưỡng đạt |
|---|---|---|---|
| 1. Tỷ lệ đồng thuận (Calibration Rate) | So sánh điểm AI chấm vs Coach chấm trên 30 bài test mẫu (Hệ thống tự tính, QA Lead kiểm tra) | 0% (Chưa có hệ thống) | ≥85% đồng thuận |
| 2. Tỷ lệ sử dụng (Adoption Rate) | Số học viên hoàn thành quiz / Tổng số học viên track Product (Hệ thống tracking log) | 0% | ≥80% (64/80 học viên) |
| 3. Tỷ lệ trượt Gate 4 (Solution) trong bài nộp FINAL | Thống kê từ bảng điểm chấm 5 Gates của Coach (Lead Coach tổng hợp) | 40% bài nộp bị trượt Gate 4 | Giảm xuống dưới 15% |
| 4. Thời gian Coach debug khái niệm trên lớp | Khảo sát nhanh (thang đo phút) với 3 Lab Coach sau buổi lab (PM nhóm G08 đo) | 15 - 20 phút/nhóm | Giảm xuống dưới 5 phút/nhóm |

   Leading indicator (biết kết quả sớm trong 1–2 tuần): Tỷ lệ hoàn thành quiz của học viên trước giờ lab (Adoption Rate) và Tỷ lệ khiếu nại/yêu cầu Coach chấm lại (tiêu chuẩn: <10% tổng số bài làm).

9. **Exit criteria** (định trước, ≥2 mức):

| Mức | Điều kiện | Hành động | Ai có quyền dừng |
|---|---|---|---|
| Cảnh báo (Yellow Flag) | Tỷ lệ học viên bấm nút "Khiếu nại/Coach chấm lại" vượt quá 15% tổng số bài làm, hoặc Calibration rate giảm xuống dưới 80%. | Tạm dừng tính năng chấm tự động Short Answer, chuyển sang chế độ chỉ hiển thị Quiz trắc nghiệm (MCQ). Nhóm G08 rà soát và tối ưu lại prompt/rubric trong 24h. | Lead Instructor / Head Coach |
| Nghiêm trọng (Red Flag) | Phát hiện AI bịa đặt kiến thức sai lệch nghiêm trọng (Hallucination) không có trong tài liệu, hoặc hệ thống bị sập/lỗi bảo mật dữ liệu. | DỪNG KHẨN CẤP toàn bộ chương trình pilot. Đóng bot/web app. Gửi thông báo đính chính và xin lỗi đến toàn bộ học viên trên Discord. | Program Lead (Sponsor) |

   *Liên hệ 2 Red Flag ở `00-context.md`*: Exit criteria trên đã chặn đứng hoàn toàn rủi ro AI chấm sai câu trả lời mở (thông qua ngưỡng khiếu nại 15%) và rủi ro bịa đặt/thiếu nguồn (thông qua Red Flag dừng khẩn cấp nếu có hallucination).

10. **Adoption** (tool không ai dùng = $0):
    - *Ai dùng đầu tiên*: 80 học viên track Product và 3 Lab Coach.
    - *Workflow đổi ở đâu*: Thay vì vào thẳng buổi lab mới tiếp cận đề bài, học viên nhận thông báo trên kênh Discord chung trước 2 ngày kèm link tham gia Quiz D28. Việc hoàn thành Quiz được quy định là "khởi động bắt buộc" trước khi đến lớp.
    - *Ai train/support*: Nhóm G08 đăng 1 video hướng dẫn siêu ngắn (1 phút) kèm tài liệu hướng dẫn trên Discord. Hỗ trợ trực tuyến 24/7 tại kênh `#ai-quiz-support`.
    - *Nếu không ai dùng thì sao*: Nếu trước giờ lab 24h mà tỷ lệ làm bài dưới 50%, hệ thống bot tự động tag tên các nhóm chưa làm trên Discord để nhắc nhở, đồng thời Lab Coach sẽ gửi tin nhắn đôn đốc trực tiếp đến các nhóm trưởng.

---

## Tự phản biện

- Budget thiếu hạng mục ẩn nào không? -> Đã tính đầy đủ chi phí API, hosting và chi phí thời gian người (human cost).
- Exit criteria đủ mạnh để THẬT SỰ dừng, hay chỉ trên giấy? -> Đã gán quyền dừng cụ thể cho Lead Instructor (mức cảnh báo) và Program Lead (mức khẩn cấp).
- Giả định quan trọng nhất sai → plan gì? -> Đã chuẩn bị phương án Fallback sang AI-assisted clustering.

---

## Tổng kiểm tra trước khi sang `2-FINAL-pitch.md`

| Hạng mục | Xong? |
|---|---|
| Tóm vấn đề trong 1 câu | [x] |
| Budget tách hạng mục, không "miscellaneous" | [x] |
| Metric có baseline + ngưỡng + ai đo | [x] |
| Exit criteria có người có quyền thực thi (≥2 mức) | [x] |
| Adoption: chỉ rõ ai dùng đầu tiên (không "cả khóa") | [x] |

⚑ Coach kiểm tra ở Mốc 4: *"Xin gì? Hứa gì? Đo gì? Dừng khi nào?"*

Sau bước này, mở `2-FINAL-pitch.md` — dồn tất cả thành 5-slide pitch + AI Support Log.

*Liên quan: handbook §A7+§A8 · `templates/ai-pilot-plan-core.md` · `prompts/06-pilot-plan-challenge.md`*
