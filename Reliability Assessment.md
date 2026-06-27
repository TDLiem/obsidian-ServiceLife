---
tags:
  - engineering-concept
  - reliability-engineering
  - statistical-models
---
## 1. Khái niệm & Thuật ngữ trung tâm

- **Độ tin cậy (Reliability - $R(t)$):** Xác suất để một linh kiện, thiết bị hoặc hệ thống thực hiện thành công chức năng quy định trong một khoảng thời gian $t$ cho trước, dưới các điều kiện môi trường vận hành/lưu kho xác định. _(Trích dẫn: MIL-HDBK-338B)_.

- **Tỷ lệ hỏng hóc (Failure Rate - $\lambda(t)$):** Tần suất xuất hiện hỏng hóc của các thiết bị còn sống sót tính trên một đơn vị thời gian.

- **Thời gian hoạt động không hỏng hóc trung bình (Mean Time To Failure - MTTF):** Áp dụng cho các thiết bị hỏng là bỏ (như đạn dược, mạch tích hợp); đối với thiết bị có thể sửa chữa, người ta dùng chỉ số **MTBF** (Mean Time Between Failures).

## 2. Công thức toán học cơ bản

### Hàm độ tin cậy lý thuyết (Phân phối lũy thừa - Tỷ lệ hỏng hóc hằng số $\lambda$):

Khi thiết bị điện tử nằm ở giai đoạn ổn định của vòng đời (đáy của đường cong chiếc bồn tắm - Bathtub Curve), hàm độ tin cậy được tính bằng:

$$R(t) = e^{-\lambda t}$$

### Phân phối Weibull (Mô hình tổng quát cho cả giai đoạn già hóa dốc xuống):

Khi hệ thống bắt đầu lão hóa mỏi cơ khí hoặc già hóa vật liệu, tỷ lệ hỏng biến thiên và đường cong độ tin cậy tuân theo:

$$R(t) = \exp \left[ - \left( \frac{t}{\eta} \right)^\beta \right]$$

**Trong đó:**

- $\beta$: Hệ số hình dáng (Shape parameter). Nếu $\beta > 1$, hệ thống đang trong giai đoạn già hóa, hao mòn theo thời gian.
    
- $\eta$: Tuổi thọ đặc trưng (Characteristic life - mốc thời gian mà tại đó 63.2% số mẫu trong lô sẽ bị hỏng).

### Công thức Nhị thức không tham số (Success-Run / Bayes cho thử nghiệm không có mẫu hỏng):

Khi thử nghiệm $n$ mẫu trong thời gian $t_{test}$ và không có mẫu nào chết ($r=0$), giới hạn dưới của độ tin cậy $R$ ở mức độ tự tin $C$ (Confidence Level) được xác định bởi:

$$R = (1 - C)^{\frac{1}{n}}$$

## 3. Các bài thử nghiệm & Phương pháp thường dùng

- **Thử nghiệm chứng minh độ tin cậy (Reliability Demonstration Testing - RDT):** Lập kế hoạch thử nghiệm (về số mẫu $n$ và thời gian test) dựa trên các biểu đồ chỉ tiêu phê duyệt/bác bỏ (_Accept/Reject criteria_) để chứng minh sản phẩm đạt mức $R$ mục tiêu trước khi nghiệm thu loạt. _(Trích dẫn: [[MIL-HDBK-781A]])_.

- **Dự đoán độ tin cậy từ dưới lên (Reliability Prediction):** * Sử dụng phương pháp **Parts Count** (Đếm linh kiện) hoặc **Parts Stress** (Phân tích ứng suất điện-nhiệt) để tính $\lambda$ tổng thể của bo mạch từ dữ liệu nền tảng của từng IC, điện trở, tụ điện. _(Trích dẫn: [[MIL-HDBK-217F]])_. Kết hợp mô hình cơ học để tính toán độ tin cậy cấu trúc phần cứng. _(Trích dẫn: [[NSWC-11]])_.  

- **Phân tích kỹ thuật an toàn hệ thống (FMECA):** Phân tích các chế độ hỏng hóc, tác động và mức độ nghiêm trọng (Failure Mode, Effects, and Criticality Analysis) để định vị xem linh kiện nào là "mắt xích yếu nhất", từ đó tập trung đo đạc sự suy giảm của chính linh kiện đó.