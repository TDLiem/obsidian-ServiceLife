---
tags:
  - engineering-concept
  - shelf-life
  - aging-kinetics
---
## 1. Khái niệm & Thuật ngữ trung tâm

- **Tuổi thọ lưu kho (Shelf Life / Storage Life):** Khoảng thời gian một thiết bị hoặc hệ thống có thể được bảo quản trong điều kiện môi trường quy định mà vẫn duy trì được các tính năng kỹ thuật và độ tin cậy thiết kế để sẵn sàng chiến đấu hoặc vận hành. _(Trích dẫn: [[NATO-AOP-48]])_.

- **Tuổi thọ vận hành (Operational Life):** Khoảng thời gian tích lũy mà thiết bị có thể hoạt động liên tục hoặc gián đoạn ở chế độ có nguồn/chạy máy trước khi chạm ngưỡng hỏng hóc.

- **Vật lý hỏng hóc (Physics of Failure - PoF):** Cách tiếp cận dựa trên bản chất cơ-điện-hóa học của vật liệu để tìm ra cơ chế gây lão hóa (như khô tụ điện, giòn cao su, khuếch tán bán dẫn) thay vì chỉ thống kê số liệu thuần túy. _(Trích dẫn: [[NATO-AOP-46]])_.

## 2. Công thức liên quan

Trong đánh giá tuổi thọ lưu kho, mô hình hiệu ứng nhiệt **Arrhenius** là công thức kinh điển nhất để tính Toán hệ số gia tốc thời gian ($AF$ - Acceleration Factor) khi nâng nhiệt độ trong tủ thử nghiệm.

## 3. Các bài thử nghiệm & Phương pháp thường dùng

- **Thử nghiệm già hóa gia tốc (Accelerated Life Testing - ALT):** Đưa các mẫu thử vào môi trường ứng suất cao _(nhiệt độ cố định hoặc chu kỳ nhiệt ẩm theo [[MIL-STD-2105E]])_ để ép quá trình lão hóa diễn ra nhanh hơn thế giới thực.

- **Phân tích quỹ đạo suy giảm tham số (Degradation Analysis):** Đo đạc các thông số nhạy cảm (dòng rò, điện áp, tần số) tại các mốc thời gian của bài test ALT. Sau đó khớp hàm toán học (tuyến tính hoặc hàm mũ) để ngoại suy thời điểm tham số chạm vạch lỗi (_Failure Threshold_).

- **Giám sát kho bãi thực tế (Stockpile Surveillance / In-Service Surveillance):** Rút mẫu ngẫu nhiên theo định kỳ từ kho chiến lược mang về phòng thí nghiệm kiểm tra không phá hủy và phá hủy để hiệu chuẩn lại mô hình dự báo lý thuyết. _(Trích dẫn: US Army AR 702-6)_.