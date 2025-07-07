# 🔐 Secure File Room

Ứng dụng chia sẻ file an toàn có giới hạn thời gian truy cập, sử dụng các kỹ thuật bảo mật nâng cao (AES, RSA, SHA-512, Chữ ký số). Giao diện trực quan, hỗ trợ gửi qua LAN hoặc mã hóa file từ Google Drive.

---

## ✨ Tính năng nổi bật

- ✅ Mã hóa file bằng AES-CBC 256-bit
- 🔐 Mã hóa khóa AES bằng RSA 2048-bit
- ✍️ Chữ ký số + SHA-512 xác thực người gửi
- ⏳ Hạn sử dụng file (24h)
- 📡 Gửi/nhận file qua LAN (Socket TCP)
- ☁️ Hỗ trợ tải file từ Google Drive để mã hóa
- 👤 Quản lý tài khoản người dùng (SHA-256)
- 🧑‍🤝‍🧑 Hệ thống Room riêng với mật khẩu
- 💬 Chat nội bộ trong Room
- 🌙 Giao diện DarkMode sử dụng `customtkinter`

---

## 🖼️ Giao diện

> Giao diện chính sau khi đăng nhập và vào phòng:

![Secure File Room GUI](https://via.placeholder.com/600x300.png?text=Giao+di%E1%BB%87n+ch%C3%ADnh)  
_(Bạn có thể chụp lại ảnh ứng dụng thật để thay thế)_

---

## ⚙️ Cài đặt

### 1. Clone repo:

```bash
git clone https://github.com/yourusername/SecureFileRoom.git
cd SecureFileRoom
SecureFileRoom/
│
├── gui_app.py                  # Giao diện người dùng (GUI)
├── server.py                   # Server LAN để nhận file
├── users.json                  # Dữ liệu người dùng (mật khẩu đã hash)
├── README.md                   # 👉 Bổ sung mô tả chi tiết
├── requirements.txt            # Danh sách thư viện Python
├── rooms/                      # Thư mục chứa các file mã hóa
├── received_packets/           # Thư mục chứa các file nhận từ LAN
├── temp/                       # Tạm thời lưu file Google Drive
└── keys/
    ├── sender_private.pem
    ├── sender_public.pem
    ├── receiver_private.pem
    └── receiver_public.pem
