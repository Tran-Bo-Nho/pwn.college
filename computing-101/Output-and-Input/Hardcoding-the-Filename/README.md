# 📜 Hardcoding the Filename – Writeup

## 🧠 Mục tiêu

Trong challenge này (pwn.college):

- Không có argument truyền vào chương trình
- Không có sẵn chuỗi `/flag` trong bộ nhớ
- Phải tự ghi chuỗi `/flag\0` lên stack
- Dùng syscall để mở, đọc và in nội dung file

---

## 👉 Mục tiêu chính

- Ghi `/flag\0` vào `rsp`
- Gọi `open`
- `read` 64 bytes
- `write` ra stdout
- `exit(42)`

---
<img width="1033" height="856" alt="image" src="https://github.com/user-attachments/assets/bd688e2c-aa23-4d2a-b7ad-c41c7aff368a" />
