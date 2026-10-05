# Prototype Feedback Note — Nguyễn Anh Dũng

MHV: 2A202602554 · Nhóm FinTech · Case A · Option A.

## 1. Bối cảnh

- Tester: một người ngoài nhóm; thông tin định danh không lưu trong bộ nộp.
- Đặc điểm quan sát được: sinh viên kỹ thuật CNTT/AI/Data Science, có xu hướng muốn tự kiểm soát cách học.
- Tình huống: ở màn chung, quiz mẫu có hai lựa chọn sai về Chunk Overlap và Top-k Retrieval.
- Task: dùng lần lượt A → B → C để tìm hỗ trợ phù hợp và quay lại bài học; quay về màn chung trước mỗi option.
- Facilitate: Nguyễn Anh Dũng.
- Ghi nhận này là một phiên test thật; nội dung được tổng hợp cùng hai phiên khác trong `group-feedback-synthesis.md`.

## 2. Hành vi quan sát được

| Nội dung | Ghi nhận |
| --- | --- |
| Hành động đầu tiên | Thử lần lượt A → B → C; ở A đọc kỹ chẩn đoán về việc làm sai quiz hai lần, sau đó chuyển sang thử các nút ở B. |
| Evidence đọc/bỏ qua | Đọc chẩn đoán và ví dụ trực quan ở A; ở C chú ý kết luận AI tập trung 80% vào Chunk Overlap. |
| Cách lấy lại control | Ở B, chủ động yêu cầu đổi cách giải thích, so sánh overlap 0 và 50, chuyển sang Top-k, rồi tự gõ sửa ghi chú cá nhân. |
| Điểm do dự / breakdown | A khá định hướng nên khó hỏi chi tiết riêng; B cho nhiều lựa chọn khiến tester phải tự quyết cách hỏi khi đang bí; C tạo lo ngại AI suy luận sai trọng tâm nhưng người học phải chủ động vào luồng ngoại lệ để sửa. |
| Kết thúc | Chọn Option B. |

## 3. Đánh giá của tester

- **Option A:** Control 4/5, Help 5/5.
  - Thích: AI chủ động phát hiện lỗi và ví dụ lợp ngói giúp hiểu nhanh Chunk Overlap.
  - Chưa hài lòng: “Luồng gợi ý ban đầu khá định hướng; muốn hỏi một chi tiết riêng thì chưa tiện.”

- **Option B:** Control 5/5, Help 5/5.
  - Thích: có thể đổi cách giải thích, so sánh overlap = 0 và 50, chuyển sang Top-k và tự chỉnh ghi chú.
  - Chưa hài lòng: “Nhiều lựa chọn can thiệp khiến tôi phải tự quyết khá nhiều; lúc đang bí kiến thức có thể không biết nên chọn cách hỏi nào trước.”

- **Option C:** Control 3/5, Help 4/5.
  - Thích: gói ôn được chuẩn bị sẵn, có thể duyệt để quay lại quiz nhanh.
  - Chưa hài lòng: “AI tự kết luận 80% lỗi nằm ở overlap khiến tôi hơi lo: nếu nguyên nhân thật sự là Top-k hoặc đọc nhầm đề thì phải chủ động vào báo ngoại lệ để sửa.”

## 4. Lựa chọn, trade-off và diễn giải

**Lựa chọn:** Option B.

**Lý do & trade-off nguyên văn:** “B phù hợp nhất khi tôi muốn hiểu đúng lỗ hổng của bản thân và có thể thay đổi cách học ngay trong lúc trao đổi. Đánh đổi là cần thêm các câu hỏi gợi ý hoặc lộ trình ngắn để người học không bị bí khi chưa biết phải yêu cầu AI hỗ trợ thế nào.”

### OBSERVED — thực tế

- Tester dùng tích cực các công cụ can thiệp ở B: đổi góc độ giải thích, so sánh, chuyển chủ đề và sửa ghi chú.
- Tester đánh giá quyền kiểm soát của B cao nhất (5/5), chọn B, đồng thời nêu rõ sự thiếu định hướng khi chưa biết bắt đầu hỏi từ đâu.
- Tester lo ngại AI kết luận quá sớm ở C và thấy A khó cho việc hỏi sâu vào một chi tiết riêng.

### INTERPRETED — từ phiên test

Người học đánh giá cao quyền điều phối của B nhưng vẫn cần các gợi ý khởi đầu ngắn để giảm áp lực nghĩ câu hỏi. Đây là tín hiệu ủng hộ cơ chế kết hợp giữa chẩn đoán ban đầu và đối thoại đào sâu, không phải bằng chứng xác nhận cho mọi người học.

### DECIDED — NEXT CHANGE của nhóm

Đề xuất hướng **Hybrid Scaffolded Drill-down**: đưa ra 2–3 câu hỏi gợi ý theo ngữ cảnh sau chẩn đoán ban đầu, đồng thời cho người học tự do hỏi sâu và tự tay quyết định trước khi áp dụng gợi ý.

### STILL UNPROVEN

- Gợi ý khởi đầu có giúp người học hoàn thành quiz trong mục tiêu dưới 10 phút không.
- Cơ chế hỏi sâu có làm người học sa đà hoặc chệch mục tiêu bài học không.
- Kết quả này có lặp lại với người mới bắt đầu hay người học dưới áp lực thời gian không.
