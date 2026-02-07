# CIRCLE_A_G – CODEX WORKFLOW
## VS CODE ↔ CODEX ↔ SYSTEM ARCHITECT

---

## 0. MỤC TIÊU
Workflow này đảm bảo:
- Codex làm việc như **Senior Engineer có kỷ luật**
- Không phá logic, không xóa code, không đổi output
- System Architect là **người quyết định cuối cùng**

---

## 1. VAI TRÒ

### 1.1. System Architect
- Quyết định kiến trúc & nghiệp vụ
- Phê duyệt hoặc từ chối thay đổi
- Khóa / mở version

### 1.2. Codex
- Đọc code và tài liệu
- Phân tích logic
- Đề xuất thay đổi **trong phạm vi cho phép**

### 1.3. VS Code / Repository
- Nơi xem diff
- Nơi review
- Nơi merge cuối

---

## 2. LUỒNG LÀM VIỆC CHUẨN

### BƯỚC A — GIAO TASK
System Architect chuẩn bị:
- CORE_RULES.md
- FORM_v1_1.yaml
- FORM_v1_1_VI.md
- CODEX_MASTER_PROMPT.md

Task phải ghi rõ:
- Mục tiêu
- Phạm vi file
- Điều cấm
- Kết quả mong đợi

---

### BƯỚC B — CODEX XỬ LÝ
Codex phải:
- Đọc toàn bộ tài liệu
- Nếu thiếu thông tin → DỪNG & HỎI
- Chỉ làm trong phạm vi cho phép
- Trả kết quả theo format bắt buộc

---

### BƯỚC C — REVIEW
System Architect:
- Xem diff từng dòng
- Kiểm tra:
  - Có xóa code không?
  - Có đổi output không?
  - Có đổi semantics không?

Không đạt → **REJECT**

---

### BƯỚC D — MERGE & LOCK
- Merge khi 100% an toàn
- Ghi rõ FORM version & Task ID
- Lock version nếu cần

---

## 3. DẤU HIỆU CODEX PHÁ LUẬT

🚨 Cảnh báo:
- “Simplified logic”
- “Removed unused code”
- Đổi tên field public
- Gộp logic không được yêu cầu

Gặp các dấu hiệu trên → **FAIL NGAY**

---

## 4. QUY TẮC VÀNG
- Không giao task mơ hồ
- Không giao nhiều mục tiêu trong 1 task
- Không merge khi còn nghi ngờ
- FORM & CORE_RULES **luôn ưu tiên hơn code**

---

## 5. TÌNH HUỐNG ĐẶC BIỆT

### 5.1. Muốn cải tiến logic
→ Tạo FORM phiên bản mới  
→ Không sửa FORM v1.1

### 5.2. Muốn xóa code
→ **KHÔNG XÓA**  
→ Chỉ deprecate

---

STATUS: ACTIVE  
FINAL AUTHORITY: SYSTEM ARCHITECT
