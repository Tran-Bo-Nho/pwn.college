# 📜 Check First Character of argv[1] – Writeup

---

## 🧠 Mục tiêu

Trong challenge này:

- Chương trình nhận **command-line argument**
- `argv[1]` là **đối số đầu tiên được truyền vào**
- Cần kiểm tra **ký tự đầu tiên của `argv[1]`**
- Nếu ký tự đầu tiên là **`'p'`** → chương trình **exit(1)**
- Nếu không phải **`'p'`** → chương trình **exit(0)**

---

## 👉 Mục tiêu chính

- Lấy **con trỏ `argv[1]` từ stack**
- Truy cập **ký tự đầu tiên của chuỗi**
- So sánh với ký tự `'p'`
- Dùng **`setz`** để lấy kết quả
- Gọi **syscall `exit`**

---

<img width="1705" height="297" alt="image" src="https://github.com/user-attachments/assets/fcfd91f6-e9c1-478a-9036-fd9897556e9b" />
