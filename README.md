# 🕳️ PoLoT - Detect Potholes

PoLoT (Pothole Locator and Tracker) là một ứng dụng Android giúp phát hiện ổ gà trên đường bằng cảm biến gia tốc của điện thoại. Ứng dụng sử dụng Mapsforge để hiển thị vị trí ổ gà theo thời gian thực và cập nhật chúng lên máy chủ Node.js thông qua API, nơi các vị trí được lưu trữ trong MongoDB.

## 🚀 Tính năng chính

- 📡 **Phát hiện ổ gà** sử dụng cảm biến Accelerometer trên điện thoại (Gia tốc kế).
- 🗺️ **Hiển thị ổ gà** trên bản đồ Mapsforge.
- 🔁 **Cập nhật thời gian thực** vị trí ổ gà lên server Node.js.
- 🧭 **Theo dõi vị trí hiện tại** của người dùng bằng GPS.
- 🧩 Giao diện trực quan, dễ sử dụng.

## 📷 Giao diện (Screenshots)
<p align="center">
  <img src="https://github.com/user-attachments/assets/991673e4-7c63-4577-bf6d-64a124443752" alt="Welcome" width="30%" />
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/f3925c75-ccea-4510-b020-bddd2544b59f" alt="Dashboard1" width="30%" />
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/d90d24a3-73de-4a80-bd88-e4bedcd6bc52" alt="Map" width="30%" />
</p>

## 📦 Kiến trúc phân lớp

![flow_syst](https://github.com/user-attachments/assets/f53d6fc6-a6d5-4550-b422-8a264e23233c)

## ⚙️ Cài đặt & chạy ứng dụng

### 🔧 Yêu cầu hệ thống

- ✅ Android Studio (Arctic Fox trở lên)
- ✅ Thiết bị Android có cảm biến **Accelerometer** và **GPS**
- ✅ Máy chủ **Node.js** đang chạy REST API
- ✅ Kết nối Internet hoặc mạng nội bộ để gửi dữ liệu đến server

---

### 📥 Hướng dẫn cài đặt

#### 1. Clone dự án từ GitHub

```bash
git clone https://github.com/<your-username>/PoLoT-DetectPotholes.git
cd PoLoT-DetectPotholes
