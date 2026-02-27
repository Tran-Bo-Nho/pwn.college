# 🔎 Trace Me – Writeup

---

## 🧠 Mục tiêu

Trong challenge này:

- Chúng ta được cung cấp một chương trình `/challenge/trace-me`
- Nhiệm vụ là theo dõi các **system call** mà chương trình thực hiện
- Tìm giá trị được truyền vào syscall `alarm`
- Submit lại giá trị đó cho `/challenge/submit-number`

👉 **Mục tiêu chính:**

- Xác định tham số của `alarm(...)`
- Submit đúng con số đó

---

## 🛠 Công cụ sử dụng

Ta dùng:

```bash
strace /challenge/trace-me
```
<img width="1305" height="241" alt="image" src="https://github.com/user-attachments/assets/8cae7d43-da3e-482c-a30f-4c0debd0210f" />
