# CIRCLE_A_G – CORE RULES (CODEX CONSTITUTION)

## 0. MỤC ĐÍCH
Tài liệu này là luật nền bất biến để Codex làm việc với dự án CIRCLE_A_G.
Mọi thay đổi, refactor, kiểm tra logic BẮT BUỘC tuân theo tài liệu này.

## 1. NGUYÊN TẮC TỐI THƯỢNG
1. Backward Compatibility > Clean Code > Optimization
2. FORM là hợp đồng, không phải gợi ý.
3. Version ở trạng thái FINAL_LOCK không được sửa logic.
4. Nếu không chắc chắn → DỪNG VÀ HỎI.
5. Không tự suy diễn nghiệp vụ.

## 2. KHÁI NIỆM BẤT BIẾN
- FORM: Định nghĩa cấu trúc dữ liệu và ràng buộc logic.
- VERSION: Phiên bản của FORM hoặc module.
- FINAL_LOCK: Trạng thái khóa tuyệt đối.
- COMPATIBILITY: Mọi thay đổi phải chạy được với hệ cũ.

## 3. CẤM TUYỆT ĐỐI
- Không được cắt bỏ logic hiện có.
- Không được xóa code đang chạy, kể cả khi có vẻ thừa.
- Logic muốn loại bỏ chỉ được deprecate hoặc bọc guard.

## 4. PHẠM VI QUYỀN CỦA CODEX
ĐƯỢC PHÉP:
- Kiểm tra logic
- Phát hiện lỗi
- Refactor không đổi output
- Thêm validation an toàn

KHÔNG ĐƯỢC PHÉP:
- Đổi kiến trúc
- Đổi FORM đã lock
- Đổi interface public
- Tối ưu làm thay đổi hành vi

## 5. QUY TẮC LÀM VIỆC
- Mỗi task = 1 mục tiêu
- Giải thích rõ mọi thay đổi
- Chỉ đề xuất, không tự quyết
- Báo rủi ro nếu có

## 6. PASS / FAIL
PASS nếu:
- Output không đổi
- Không xóa code
- Tuân FORM

FAIL nếu:
- Phá compatibility
- Suy diễn nghiệp vụ
- Tự ý đổi logic

## 7. MỆNH LỆNH BẮT BUỘC
Nếu thiếu thông tin hoặc logic không rõ → PHẢI DỪNG VÀ HỎI.
