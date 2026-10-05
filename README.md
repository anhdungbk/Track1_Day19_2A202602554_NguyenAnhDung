# Track1_Day19_2A202602554_NguyenAnhDung

## 1. Thông tin cá nhân và nhóm

- Họ tên: Nguyễn Anh Dũng.
- MHV: 2A202602554.
- Nhóm: FinTech.
- Thành viên: Nguyễn Anh Dũng, Tạ Việt Cường, Nguyễn Văn Thăng.
- Case: Case A — AI Tutor: Diagnostic Refresher.
- Option phụ trách: A — AI gợi ý dẫn dắt: người học kích hoạt, xem chẩn đoán và chọn chấp nhận, đổi trọng tâm hoặc từ chối.
- Phân công chung: Cường phụ trách B và màn chung; Thăng phụ trách C.

## 2. Hypothesis Problem

> Khi đang học bài mới trên VLearn và bị mắc ở nội dung chưa hiểu hoặc quiz trả lời sai, người học gặp khó khăn trong việc tìm đúng nội dung cần ôn để tiếp tục vì chưa xác định được khái niệm liên quan đến điểm mắc, dẫn đến tìm qua nhiều nguồn và có thể trì hoãn hoặc bỏ dở việc học.

Đây là giả thuyết cần nghiên cứu tiếp. Note Cường nêu một trường hợp tìm nhiều nguồn và bỏ dở; note Thăng nêu khó xác định phần cần xem lại. Note Day17 của tôi có lời kể thời gian thường 1–2 phút khi hỏi AI (02:29), nên không coi mọi lần chưa hiểu đều tốn nhiều công hoặc do thiếu kiến thức nền.

Chi tiết evidence và thiết kế: [three-option-design-sheet.md](three-option-design-sheet.md).

## 3. Three Solution Options

| Option | Cơ chế | Người phụ trách |
| --- | --- | --- |
| A | Sau khi người học kích hoạt, AI chẩn đoán từ hai câu quiz sai và dữ liệu mẫu; người học chấp nhận, đổi sang Top-k hoặc từ chối gợi ý | Nguyễn Anh Dũng |
| B | Đối thoại hai chiều: người học điều phối cách AI giải thích, chuyển chủ đề và tự sửa ghi chú | Tạ Việt Cường |
| C | AI tự soạn gói ôn ngầm; người học duyệt áp dụng hoặc báo ngoại lệ để thu hồi tự động hóa | Nguyễn Văn Thăng |

Cả ba dùng cùng màn RAG, quiz mẫu và nhiệm vụ tìm hỗ trợ để quay lại bài. Mở [prototype/index.html](prototype/index.html) để trải nghiệm; Option A nằm tại [prototype/option-a.html](prototype/option-a.html). Thông tin truy cập: [prototype-link.md](prototype-link.md).

## 4. Đóng góp của tôi trong nhóm

Trong bộ nộp này, tôi phụ trách thiết kế và hoàn thiện Option A với AI hỗ trợ:
- Thiết kế luồng hai trạng thái: người học chủ động kích hoạt trước, sau đó xem chẩn đoán và ra quyết định.
- Dùng hai câu quiz sai cùng dữ liệu lịch sử mẫu để giải thích vì sao AI ưu tiên Chunk Overlap; không dùng dữ liệu cá nhân thật.
- Cung cấp ba đường kiểm soát: chấp nhận gợi ý, đổi trọng tâm sang Top-k, hoặc từ chối và tự học.
- Bổ sung đường quay lại trạng thái trước kích hoạt và Trang chủ để người học phục hồi luồng học.
- Hiển thị tín hiệu chẩn đoán và giới hạn nhận định bằng dữ liệu mẫu.
- Tổ chức Design Sheet, hướng dẫn test và AI Support Log cá nhân.
