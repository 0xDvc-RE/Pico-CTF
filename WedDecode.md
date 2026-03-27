<img width="932" height="807" alt="image" src="https://github.com/user-attachments/assets/8a3d36e8-f023-4846-91b4-79ca55b50b2c" />

Hints:

1: Hãy sử dụng công cụ Web Inspector trên các tệp khác được trang web tải kèm.

2: Flag có thể đã được mã hóa hoặc cũng có thể không.



<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/b766493f-358d-4e5a-af8d-06aa0bd50c1f" />



Trong bài này mình phải đi xác định đoạn mã lạ vì đó có thể là flag đang bị encode. 

Bài này có thể dùng BurpSite để hỗ trợ nhưng mình sẽ làm đơn giản hơn. 

Mình sử dụng trực tiếp Ctrl+U để thăm dò trong source code từng menu.


<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/77b0a41d-1827-4c12-991f-5b44f97642ad" />

Ở Home mình không thấy có gì bất thường

<img width="1919" height="962" alt="image" src="https://github.com/user-attachments/assets/91fb7026-7ce1-4bc9-88f4-93905aec7281" />

Mình tiếp tục kiểm tra trong contact cũng không có gì lạ

<img width="1917" height="976" alt="image" src="https://github.com/user-attachments/assets/becadce2-3a2a-4b20-af09-87c8b54a0c21" />

Vậy chỉ còn About và mình đã tìm thấy đoạn mã kì lạ ở đây.

Mình sẽ đưa nó sang Base64 decode 


<img width="1919" height="967" alt="image" src="https://github.com/user-attachments/assets/0d15ee66-c503-4da4-9ec7-6f6daf3f4f46" />

Sau khi decode mình đã có flag cần tìm.
