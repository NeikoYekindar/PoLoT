# 🚧 PoLoT - Server ứng dụng

Đây là server của ứng dụng **PoLoT** phục vụ cho việc lưu trữ, cung cấp thông tin, kết nối người dùng với nhau. Mỗi khi ổ gà được ghi nhận từ ứng dụng gửi về server để lưu trữ vàvà xây dựng bản đồ cảnh báo ổ gà.

## Các tính năng chính Server

### 👤 Xác thực người dùng (Auth)

- <strong>Đăng kí/Đăng nhập</strong>
  - người dùng tạo tài với email và password
  - Ngoài ra còn đăng nhập thông qua tài khoản **Google** và **Facebook**.
- <strong>Quên mật khẩu</strong>
  - Gửi mã OTP về email đã đăng ký để xác minh
  - Đặt lại mật khẩu thông qua mã OTP
- <strong>Token</strong>
  - Sử dụng **JWT** để xác thực người dùng sau khi đăng nhập
  - Token được lưu trữ cục bộ trên ứng dụng và gửi kèm các request

### 🚗 Phát hiện ổ gà

- Thu thập dữ liệu từ **cảm biến gia tốc (accelerometer)** trên điện thoại.
- Nhận diện ổ gà dựa trên ngưỡng dao động bất thường.
- Ghi lại tọa độ GPS, thời gian và phân loại ổ gà.
- Gửi thông tin về server qua RESTful API

## 🌐 Backend Server

### 🧰 Công nghệ sử dụng

- **Ngôn ngữ:** Nodejs
- **Framework:** Express.js
- **Cơ sở dữ liệu:** MongoDB
- **Xác thực:** JWT, Google OAuth2, Facebook Login

### 🔐 API xác thực

| Phương thức | Endpoint                     | Mô tả                           |
| ----------- | ---------------------------- | ------------------------------- |
| `POST`      | `/api/users/register`        | `Đăng kí tài khoản`             |
| `POST`      | `/api/users/login`           | `Đăng nhập bằng email/pasword`  |
| `POST`      | `/api/user/google-sign-in`   | `Đăng nhập bằng Google`         |
| `POST`      | `/api/user/facebook-sign-in` | `Đăng nhập bằng FFacebook`      |
| `POST`      | `/api/user/forgot-pasword`   | `Gửi OTP đến email`             |
| `POST`      | `/api/user/verify`           | `Xác thực OTP`                  |
| `PUT`       | `/api/user/edit`             | `Thay đổi thông tin người dùng` |

### Triển khai lên VPS

Sử dụng [Dockerfile](https://github.com/LongLeeeee/NT118.P12/blob/main/nodejs_server/Dockerfile) để build ra image.

```sh
docker build -t abc/polot:latest .
```

Sau khi build thành công, ta sẽ push image vừa tạo lên một Registry nào đó - ở đây chọn Docker Hub.

```sh
docker push abc/polot:latest
```

- Lưu ý: trước khi push phải login trên máy local.

Truy cập vào VPS, tiến hành pull image về và run container.

```sh
docker run -d -p 8000:8000 --env-file .env abc/polot:latest
```
