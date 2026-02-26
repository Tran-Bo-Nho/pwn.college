# Moving Between Registers – Writeup

## 🧠 Mục tiêu

Trong challenge này:

- Giá trị bí mật được lưu trong thanh ghi `rsi`
- Chương trình phải `exit` với giá trị đó làm return code
- Nhưng syscall `exit` lấy giá trị return từ thanh ghi `rdi`

👉 Vì vậy ta cần **chuyển giá trị từ `rsi` sang `rdi`**

<img width="445" height="190" alt="image" src="https://github.com/user-attachments/assets/dcd4cc2b-20c8-4e8a-bc58-5f6373c18f6e" />


<img width="1708" height="804" alt="image" src="https://github.com/user-attachments/assets/160b6a92-9a88-4605-a6d5-67c03cd9d990" />
