# 🧵 Argument On The Stack – Writeup

---

## 🧠 Mục tiêu

Trong challenge này:

- Chương trình `/challenge/debug-me` được cung cấp  
- FLAG được truyền vào làm **argument đầu tiên**  
- Nhiệm vụ là đọc flag trực tiếp từ stack bằng `gdb`

---

## 👉 Mục tiêu chính

- Lấy địa chỉ của `argv[1]` từ stack  
- Dereference để đọc nội dung chuỗi  
- Thu được flag  

---

## 🛠 Công cụ sử dụng & Lệnh thực hiện

Chạy chương trình với `gdb`:

```bash
gdb /challenge/debug-me
```

Start chương trình:

```bash
starti
```

Lấy địa chỉ của argument đầu tiên (`argv[1]`):

```bash
x/a $rsp+16
```

Đọc nội dung chuỗi tại địa chỉ vừa lấy được:

```bash
x/s <address>
```
