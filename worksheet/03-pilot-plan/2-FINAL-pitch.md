---
artifact: 8 — 5-slide Pitch + AI Support Log (bản nộp cuối lab)
bai-tap: Pilot Plan — dồn thành pitch, sẵn sàng phản biện
phase: Double Diamond vòng 2 · ◆ output (bản nộp cuối + present)
time: ~5 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-pilot-plan.md + toàn bộ 01-frame + 02-solution · templates/5-slide-pitch.md
nop-cuoi: Có — bản nộp cuối lab (Part E · 5-slide Pitch + AI Support Log)
---

# 2 — FINAL: 5-slide Pitch + AI Support Log

Mục tiêu: dồn cả A3 Working Canvas thành 5 slide pitch (5 phút), chuẩn bị trả lời 3 câu phản biện, và ghi AI Support Log. Đây là bản nộp cuối cùng của lab.

Lý do làm bước này: nguyên tắc *demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu*. Slide đẹp mà không trả lời được "số này lấy ở đâu" thì hỏng. Pitch không phải kể chuyện — là đưa evidence để stakeholder ra được một quyết định.

Quy tắc: **slide cuối phải là một lời xin rõ ràng** (xin gì · đổi lại hứa gì). Không có lời xin = stakeholder không biết approve cái gì.

## Quy trình 5 phút

```text
3 phút  — Dồn 5 slide (mỗi slide 1 thông điệp)
1 phút  — Chuẩn bị 3 câu phản biện
1 phút  — AI Support Log
```

---

## Phần A — 5 slide (mỗi slide 1 thông điệp)

Kéo nguyên liệu từ các file đã làm, đừng viết mới. Khung đầy đủ: `templates/5-slide-pitch.md`.

| # | Slide | Lấy từ | Nội dung 1–2 gạch đầu dòng | Ai nói |
|---|---|---|---|---|
| 1 | Problem & user | 01-frame/3-FINAL | • **Nỗi đau thực chiến**: 65% học viên track Product (~80 người) bước vào Lab D28 mà chưa hiểu rõ bản chất Build/Buy/Boost, khiến 3 Lab Coach lãng phí ~6.75 giờ giải thích khái niệm cơ bản và 40% bài nộp FINAL bị trượt Gate 4.<br>• **Mục tiêu**: Chuẩn hóa kiến thức và triệt tiêu hiểu lầm trước giờ lab để Coach tập trung góp ý chiến lược sâu. | Trịnh Uyên Chi |
| 2 | Breakdown & Quick Win | 01-frame/1,2 | • **Giải pháp bóc tách**: Thay vì xây dựng cả hệ thống Learning OS cồng kềnh, nhóm chọn đúng 1 Quick Win cho riêng Day 28: Hệ thống Quiz & Auto Grading (Tạo quiz 10 câu, chấm Short Answer, phát hiện misconception và gợi ý tài liệu học lại).<br>• **Lý do chọn**: Tác động tức thì (Impact 5/5), chứng minh giá trị ngay trong 1 tuần pilot, được sự ủng hộ mạnh mẽ từ Head of Academic và đội ngũ Lab Coach. | Trịnh Uyên Chi |
| 3 | Solution + bản vẽ trực quan | 02-solution/2-FINAL | • **Chiến lược Boost**: Sử dụng Gemini 1.5 Pro API kết hợp RAG tài liệu D28 và Few-shot Prompting qua Discord bot/Web app. Chi phí cực rẻ (~$25), không lãng phí nguồn lực để "tự build từ số 0".<br>• **Trực quan & Kiểm soát**: AI xuất kết quả JSON chuẩn (Điểm, Lỗi sai, Trích dẫn gốc trang sách). Có nút [Báo cáo Coach chấm lại] để đảm bảo Human-in-the-loop tuyệt đối. | Lê Hoàng Long |
| 4 | AI Pilot Plan | 03-pilot-plan/1 | • **Kế hoạch triển khai (1 tuần pilot)**: Phase 1 (3 ngày) chạy Benchmark 30 bài mẫu để Lead Instructor nghiệm thu (Calibration ≥85%); Phase 2 (4 ngày) mở rộng cho 80 học viên track Product sử dụng trước giờ lab.<br>• **Adoption & Bảo mật**: Tích hợp thẳng vào luồng Discord quen thuộc, quy định làm quiz là bước khởi động trước lab, cam kết bảo mật dữ liệu qua API thương mại. | Nguyễn Phạm Trà My |
| 5 | Metric · exit criteria · **lời xin** | 03-pilot-plan/1 | • **Cam kết đo lường**: Đạt ≥80% adoption rate, giảm tỷ lệ trượt Gate 4 xuống <15%, giảm thời gian giải thích của Coach xuống <5 phút/nhóm.<br>• **Exit Criteria rõ ràng**: Dừng tự động chấm nếu tỷ lệ khiếu nại >15% (Yellow Flag); Dừng khẩn cấp toàn bộ pilot nếu AI bịa đặt kiến thức (Red Flag).<br>• 🎯 **LỜI XIN**: Xin cấp ngân sách **$25** tiền mặt (chi phí API & Server) và **3 giờ công** của Lead Instructor để duyệt bộ prompt/rubric. Đổi lại, nhóm cam kết bàn giao hệ thống chạy mượt mà và báo cáo Top 3 misconceptions của lớp trước giờ học live Day 28! | Nguyễn Phạm Trà My |

## Phần B — Chuẩn bị 3 câu phản biện

Business owner/instructor sẽ hỏi mỗi nhóm 1–2 câu. Viết sẵn câu trả lời:

1. *"Số liệu / giả định này lấy ở đâu?"* → 
```text
Số liệu về 65% học viên hiểu sai Build/Buy/Boost và 40% bài nộp trượt Gate 4 được nhóm tổng hợp dựa trên quan sát thực tế và phỏng vấn ngẫu nhiên các Lab Coach từ các khóa AI20k trước. Chi phí API $15 được tính toán chính xác dựa trên bảng giá Gemini 1.5 Pro ($1.25/triệu token) cho 80 học viên × 3 lượt làm bài kèm RAG context.
```
2. *"Nếu giả định quan trọng nhất của bạn sai thì sao?"* → 
```text
Giả định quan trọng nhất là "LLM đủ thông minh để chấm Short Answer khớp với ý Coach (Calibration ≥85%)". Nếu giả định này sai (trong Phase 1 benchmark, AI chấm lệch quá nhiều), nhóm sẽ lập tức chuyển sang phương án dự phòng (Fallback): Sử dụng AI để gom nhóm các câu trả lời tương đương (Clustering), sau đó Coach chỉ cần chấm 1 câu đại diện cho cả nhóm. Điều này vẫn giúp tiết kiệm 80% thời gian cho Coach mà đảm bảo độ chính xác 100%.
```
3. *"Tình huống nào sẽ khiến bạn dừng pilot?"* → 
```text
Nhóm cam kết thực thi 2 mức dừng: (1) Tạm dừng tính năng chấm tự động Short Answer (chỉ giữ trắc nghiệm) nếu tỷ lệ học viên bấm nút khiếu nại vượt quá 15% tổng số bài làm; (2) Dừng khẩn cấp toàn bộ hệ thống ngay lập tức nếu phát hiện AI có hiện tượng Hallucination (bịa đặt kiến thức sai lệch không có trong handbook) hoặc xảy ra sự cố bảo mật dữ liệu.
```

## Phần C — AI Support Log

| Câu hỏi | Trả lời |
|---|---|
| AI giúp được gì trong lab này? | AI (Gemini 3 Flash) hỗ trợ nhóm đóng vai chuyên gia EdTech để nghiên cứu các tiền lệ thành công (Khanmigo, Gradescope), cấu trúc hóa luồng RAG + JSON output, và rà soát ngữ pháp/lập luận cho các slide pitch. |
| AI đưa output nào nghe hợp lý nhưng nhóm phải sửa? | Ban đầu AI đề xuất tự huấn luyện (fine-tune) một mô hình Llama-3 riêng để chấm bài cho bảo mật và chuyên nghiệp. Nhóm đã bác bỏ và sửa lại thành chiến lược "Boost" (dùng Gemini API + RAG) vì nhận thấy fine-tune quá đắt đỏ, mất thời gian và vi phạm ràng buộc ngân sách nhỏ của đề bài. |
| Phần nào nhóm tự lập luận, KHÔNG copy AI? | Toàn bộ việc lựa chọn Quick Win (tập trung vào misconception Build/Buy/Boost của Day 28), tính toán chi phí thực tế $25, thiết lập các ngưỡng Exit Criteria (15% khiếu nại) và cam kết lời xin ở slide cuối đều do nhóm tự thảo luận và quyết định dựa trên bối cảnh thực tế của khóa học AI20k. |

---

## Tổng kiểm tra trước khi nộp

| Hạng mục | Xong? |
|---|---|
| 5 slide, mỗi slide 1 thông điệp, đã phân ai nói slide nào | [x] |
| Slide 5 có lời xin rõ ràng (xin gì · hứa gì) | [x] |
| Có câu trả lời sẵn cho cả 3 câu phản biện | [x] |
| AI Support Log điền đủ 3 dòng | [x] |
| Tất cả file worksheet/ đã commit + push, link dán vào Discord | [x] |

Đây là file cuối. Pitch 5 phút + nhận phản biện theo bảng 5 Gate (`templates/rubric-gate-sheet.md`).

*Liên quan: handbook §A9 · `templates/5-slide-pitch.md` · `templates/ai-support-log.md`*
