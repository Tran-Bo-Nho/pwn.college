# assembly-note

- *Register*

| Thanh ghi | Dùng để làm gì trong pwn |
|---------- |-------------------------|
|   EIP     | Địa chỉ lệnh đang chạy → overwrite để chiếm quyền |
|   ESP     | Đỉnh stack → ROP, ret2libc phụ thuộc vào nó |
|   EBP     | Stack frame → tính offset, leak stack |

| **Thanh ghi** |     **Vai trò thực tế**         |
|-------------- | --------------------------------|
|     EAX       | Giá trị trả về của hàm / syscall|

>EIP : chiếm
>
>ESP : điều khiển
>
>EAX : Tận dụng
