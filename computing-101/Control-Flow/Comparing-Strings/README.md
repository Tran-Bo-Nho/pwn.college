# 📜 Check String `"pwn"` in argv[1] – Writeup

---

# 🧠 Mục tiêu

Trong challenge này:

* Chương trình nhận **command-line argument**
* `argv[1]` là **đối số đầu tiên được truyền vào**
* Cần kiểm tra xem chuỗi nhập vào **có bắt đầu bằng `"pwn"` hay không**
* Nếu chuỗi bắt đầu bằng `"pwn"` → chương trình `exit(0)`
* Nếu không đúng → chương trình `exit(1)`

---

# 👉 Mục tiêu chính

* Lấy con trỏ `argv[1]` từ **stack**
* Truy cập từng ký tự trong chuỗi
* So sánh từng byte với `"p"`, `"w"`, `"n"`
* Nếu có ký tự sai → nhảy tới `fail`
* Nếu tất cả đúng → chương trình `exit(0)`

---
<img width="732" height="522" alt="image" src="https://github.com/user-attachments/assets/93a681c1-389c-4288-9355-bf7768494d39" />
