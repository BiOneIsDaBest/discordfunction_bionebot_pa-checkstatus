# 🤖 BiOneBot – Discord Utility Bot

BiOneBot là một dự án bot Discord cá nhân được phát triển bằng **Python** (thư viện `discord.py`) với mục tiêu cung cấp các tính năng hỗ trợ quản lý và tiện ích cho server Discord.

---

## 🧩 Chức năng hiện có

### ⚙️ `checkstatus.py`
Module này nằm trong thư mục `cogs/`, chịu trách nhiệm **xác nhận trạng thái làm việc của nhân viên (onduty)** và **tự động offduty nếu không xác nhận đúng hạn**.

#### 🔹 Tính năng chính:
- Gửi tin nhắn xác nhận trạng thái online mỗi **3 tiếng** vào kênh `#1429695494124208169`.
- Nếu nhân viên **không bấm nút xác nhận trong 3 phút**, hệ thống sẽ tự động **offduty**.
- Nếu auto offduty, hệ thống **xóa dữ liệu giờ làm việc trong ngày đó**.
- Nếu người dùng **offduty thủ công**, dữ liệu vẫn được ghi bình thường.

---

## 🚀 Cách chạy bot

### 1️⃣ Cài đặt môi trường
Đảm bảo bạn đã cài đặt **Python 3.10+** và **pip**.

```bash
pip install -r requirements.txt
```

> Nếu chưa có file `requirements.txt`, bạn có thể tạo bằng lệnh:
> ```bash
> pip freeze > requirements.txt
> ```

---

### 2️⃣ Tạo file `.env` để lưu token bot

Tạo file `.env` trong thư mục gốc và thêm dòng sau:

```
DISCORD_TOKEN=your_bot_token_here
```

> ⚠️ Không public file `.env` lên GitHub để bảo mật token.

---

### 3️⃣ Chạy bot
```bash
python main.py
```

Nếu chỉ muốn test riêng module `checkstatus.py`:
```bash
python -m cogs.checkstatus
```

---

## 🧠 Cấu trúc dự án

```
BiOneBot-pa/
├── cogs/
│   ├── checkstatus.py      # Hệ thống xác nhận và auto offduty
│   ├── duty.py             # Quản lý giờ làm việc
│   ├── subtime.py          # Hỗ trợ tính toán thời gian
│   ├── owner.py, myinfo.py, notice.py, teach_menu.py
├── main.py                 # File khởi động bot
├── .env                    # Token bí mật
├── requirements.txt        # Thư viện cần thiết
└── README.md               # Mô tả dự án
```

---

## 💡 Hướng phát triển tiếp theo
- Tích hợp lịch làm việc và thông báo hàng tuần.
- Gửi thống kê tổng hợp thời gian on/off duty.
- Kết hợp dashboard web để quản lý dữ liệu nhân viên.

---

## 👨‍💻 Tác giả
**BiOneIsDaBest**  
📍 Melbourne, Australia  

---

## 🛡️ Bản quyền
Bản quyền thuộc **BiOneIsDaBest**  
📌 Nếu mượn sử dụng hoặc chỉnh sửa, vui lòng **ghi rõ nguồn** hoặc Liên hệ: [Discord: BiOneIsDaBest](https://discord.com/users/1146990393167200276)
