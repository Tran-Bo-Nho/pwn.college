# 🧩 Jump Table Reverse Engineering – Writeup

---

# 🧠 Mục tiêu

Trong challenge này:

• Chương trình đọc **1 byte input** từ người dùng  
• Giá trị byte này được dùng làm **index vào jump table**  
• Jump table chứa **256 địa chỉ code khác nhau**

Luồng chương trình:

• Đọc ký tự input  
• Chuyển ký tự thành **giá trị ASCII (0–255)**  
• Dùng giá trị đó để **index vào bảng địa chỉ**  
• Nhảy tới địa chỉ tương ứng bằng `jmp`

Điều đặc biệt:

• **255 entries trong jump table giống nhau**  
• **1 entry khác biệt** dẫn tới đoạn code in flag

---

# 👉 Mục tiêu chính

• Xác định **địa chỉ jump table** trong chương trình  
• Xem **256 entries trong bảng**  
• Tìm **entry có địa chỉ khác với các entry còn lại**  
• Tính **index của entry đó**  
• Chuyển index sang **ASCII character**  
• Nhập ký tự đó để chương trình nhảy tới **case in flag**

---

# 🔬 Phân tích Assembly
<img width="1034" height="1081" alt="image" src="https://github.com/user-attachments/assets/2e654853-95dc-485d-ba64-962cd0044c8c" />
• Bên trái là address entry, bên phải là entry<là địa chỉ sẽ jump tới>

• Address entry = Địa chỉ ban đầu + index * 8

<img width="954" height="212" alt="image" src="https://github.com/user-attachments/assets/16c3362e-5142-42bd-b25e-db7cf65523b5" />
• Dòng 2 là cho RAX = 0

• Dòng 3 : gán index cho 8bit cuối của rax 

• Dòng 4 : Tìm entry < địa chỉ sẽ jmp tới >
