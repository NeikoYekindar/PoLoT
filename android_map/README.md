# 📍 PoLoT Android Map

Đây là module Android của dự án PoLoT, cung cấp các tính năng bản đồ và định vị cho ứng dụng.

## 🚀 Tính năng chính

- Hiển thị bản đồ tương tác
- Định vị vị trí hiện tại của người dùng
- Thêm và quản lý các điểm đánh dấu (marker) trên bản đồ
- Tính toán và hiển thị tuyến đường giữa hai điểm

## 🛠️ Cài đặt

1. Clone repository:
   ```bash
   git clone https://github.com/NeikoYekindar/PoLoT.git
2. Mở project trong Android Studio.

## 📷 Ảnh minh họa

<p align="center">
  <img src="https://github.com/user-attachments/assets/077d8ea0-f9fe-444d-8750-70e31199b2fd" alt="Welcome" width="30%" />
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/55e743c7-c1b5-465a-baba-942ecee30c7d" alt="Dashboard1" width="30%" />
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/870bcb19-df5b-435a-bfc9-4f456c059fb4" alt="Map" width="30%" />
</p>


## ⚙️ Flow hoạt động

![Group 9019](https://github.com/user-attachments/assets/c01c5cf8-7ffb-47f2-8d13-f59b88e7a946)

1. Người dùng mở ứng dụng, bản đồ sẽ tự động hiển thị vị trí hiện tại bằng GPS.
2. Các điểm đánh dấu (markers) được tải từ backend hoặc thêm thủ công vào bản đồ.
3. Người dùng có thể nhấn vào một marker để xem chi tiết hoặc bắt đầu điều hướng.
4. Nếu người dùng chọn một điểm đích, ứng dụng sẽ gửi yêu cầu tuyến đường (route) đến OSRM server hoặc API tương ứng.
5. Tuyến đường được vẽ lên bản đồ và người dùng có thể theo dõi chỉ đường trong thời gian thực.


