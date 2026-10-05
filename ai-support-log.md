# AI Support Log — Nguyễn Anh Dũng
MHV 2A202602554 · Nhóm FinTech · Case A · Option A.

## 1. Phạm vi hỗ trợ

AI hỗ trợ khám phá cơ chế, chuyển slide sang HTML ở bước thử ban đầu, đọc bộ nhóm, hoàn thiện Option A hỏi hai câu, kiểm tra quy tắc phản hồi và tổ chức bộ nộp cá nhân.

## 2. Nhật ký prompt thực tế

Các yêu cầu dưới lấy từ cuộc trò chuyện, có trích rút gọn bằng dấu “…”. Không bổ sung ngày giờ hoặc prompt chưa từng sử dụng.

| Prompt của tôi | Kết quả AI hỗ trợ | Điều chỉnh / giới hạn |
| --- | --- | --- |
| “Hãy thử suy nghĩ phát triển 1 cơ chế… tạo 1 tab html” | Bản user-led chọn từ khóa trên slide | Chỉ là hướng khám phá ban đầu |
| “Sửa lại sau khi chọn từ cần giải thích thì nhảy luôn sang phần ‘giải thích mẫu’…” | Bỏ màn xác nhận dư | Giảm một bước ở thử nghiệm từ khóa |
| “Option A prototype/option-a.html - AI hỏi 2 câu rồi đoán, nhớ giữ nút Bỏ qua/Sửa/Quay lại ngay…” | Làm rõ cơ chế A mới theo nhóm | Không tiếp tục gọi bản từ khóa là A trong bộ nộp này |
| “Hãy đọc phần prototype và làm option A.html của tôi” | Hoàn thiện hai câu, bốn nhánh phản hồi và control | Giữ dữ liệu mô phỏng; không gọi model/API |
| “Hãy sửa lại… thành tên của tôi: Nguyễn Anh Dũng - 2A202602554…” | Tổ chức đúng bộ nộp cá nhân | Không chuyển đóng góp B/C hoặc feedback của Cường thành của tôi |

