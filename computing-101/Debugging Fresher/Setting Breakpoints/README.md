# 📜 Find Random Value on Stack – Writeup

---

## 🧠 Mục tiêu

Trong challenge này:

- Chương trình thông báo đã “set random value”
- Giá trị này được cho là nằm trên **stack**
- Nhiệm vụ:
  - Tìm giá trị đó bằng GDB
  - Hiểu rõ bản chất của nó

---

## 👉 Mục tiêu chính

- Quan sát stack bằng GDB
- Xác định vị trí giá trị nghi là “random”
- Kiểm tra xem đó có thực sự là random của chương trình không

---

## 🔍 Phân tích

Sử dụng:

```gdb
break main
run
display/8gx $rsp
```
Display dùng để tự in ra $rsp sau mỗi lệnh như nexti, stepi, ...

Khi thấy giá trị random và lần lên là sau lệnh call read, có thể ko phải do read sinh ra mà do khoảng quét rsp hơi ít nên có thể xuất hiện từ trước mà ko quét đến

Nếu khi áng được sau lệnh nào có thể sẽ xuất hiện random value có thể break, continue đến địa chỉ đó luôn
