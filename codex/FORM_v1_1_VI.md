# CIRCLE_A_G – FORM BÁO CÁO PHÂN TÍCH GIÁ VÀNG
## PHIÊN BẢN 1.1 – FINAL_LOCK (BẢN TIẾNG VIỆT CHÍNH THỨC)

---

## 0. TUYÊN BỐ HIỆU LỰC
Tài liệu này là FORM tiếng Việt chính thức của CIRCLE_A_G – phiên bản 1.1.  
FORM này có giá trị ràng buộc kỹ thuật và nghiệp vụ, tương đương 100% với bản machine-readable.

Mọi hệ thống, module, AI (bao gồm Codex) hoặc con người khi làm việc với FORM này **BẮT BUỘC TUÂN THỦ**.

---

## 1. THÔNG TIN ĐỊNH DANH
- **Tên FORM**: BÁO CÁO PHÂN TÍCH GIÁ VÀNG
- **Mã FORM**: GOLD_ANALYSIS_REPORT
- **Phiên bản**: 1.1
- **Trạng thái**: FINAL_LOCK
- **Chủ sở hữu**: SYSTEM ARCHITECT

---

## 2. MỤC ĐÍCH FORM
FORM này định nghĩa cấu trúc dữ liệu, ràng buộc logic và hành vi hệ thống cho báo cáo phân tích giá vàng dựa trên dữ liệu đã lưu trữ.

FORM là **hợp đồng bất biến** giữa các module trong CIRCLE_A_G.

---

## 3. DỮ LIỆU ĐẦU VÀO (INPUT)

### 3.1. Nguồn dữ liệu thị trường
- **Tên**: gold_market_data  
- **Loại**: Chuỗi dữ liệu theo thời gian (time series)  
- **Bắt buộc**: Có  
- **Ý nghĩa**: Dữ liệu giá vàng lịch sử dùng cho phân tích

### 3.2. Tham số phân tích
- **Tên**: analysis_window  
- **Kiểu dữ liệu**: Số nguyên  
- **Bắt buộc**: Có  
- **Ý nghĩa**: Số phiên / khoảng thời gian dùng để tính toán

---

## 4. DỮ LIỆU ĐẦU RA (OUTPUT – HỢP ĐỒNG CỐT LÕI)

### 4.1. Giá vàng hiện tại
- **Field**: gold_price  
- **Kiểu dữ liệu**: Số thực (float)  
- **Bắt buộc**: Có  
- **Ý nghĩa**: Giá vàng tại thời điểm tạo báo cáo

### 4.2. Xu hướng giá
- **Field**: trend  
- **Kiểu dữ liệu**: Chuỗi  
- **Giá trị hợp lệ**:
  - UP – Xu hướng tăng
  - DOWN – Xu hướng giảm
  - SIDEWAYS – Đi ngang
- **Bắt buộc**: Có

### 4.3. Độ biến động
- **Field**: volatility  
- **Kiểu dữ liệu**: Số thực  
- **Bắt buộc**: Có  
- **Ý nghĩa**: Mức độ dao động giá trong khoảng phân tích

### 4.4. Điểm tin cậy
- **Field**: confidence_score  
- **Kiểu dữ liệu**: Số thực  
- **Giá trị cho phép**: từ 0.0 đến 1.0  
- **Bắt buộc**: Có  
- **Ý nghĩa**: Độ tin cậy của kết quả phân tích

---

## 5. RÀNG BUỘC LOGIC BẮT BUỘC

1. **Không được xóa hoặc đổi tên field**  
   Mọi field đã định nghĩa trong FORM này là bất biến.

2. **Bắt buộc tương thích ngược (Backward Compatibility)**  
   Mọi thay đổi kỹ thuật phải đảm bảo dữ liệu và module cũ vẫn hoạt động.

3. **Bảo toàn logic hiện có**  
   - Ng
