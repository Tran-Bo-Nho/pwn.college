# 🔍 Disassemble Me – Writeup

---

## 🧠 Mục tiêu

Trong challenge này:

- Chúng ta được cung cấp một **binary có sẵn**
- Không chạy thử để đoán
- Mà phải **disassemble** để đọc mã assembly bên trong

👉 Mục tiêu chính:

- Tìm **giá trị được nạp vào thanh ghi `rdi`**
- Nhưng giá trị này **bị ghi đè (overwrite)** ngay sau đó
- Submit lại giá trị ban đầu đó

---

## 🛠 Công cụ sử dụng

Ta dùng:

```bash
objdump -d -M intel /challenge/disassemble-me
```
<img width="1611" height="462" alt="image" src="https://github.com/user-attachments/assets/cb9d33e0-b437-4fc5-8dca-984d4200c303" />
