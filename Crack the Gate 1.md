
<img width="964" height="954" alt="image" src="https://github.com/user-attachments/assets/6701653d-83e6-4584-9b64-e135d560e112" />

Hints:

1: Dev đôi khi để lại ‘hint’ trong code, nhưng không phải lúc nào cũng để lộ rõ ràng.

2: Một cách mã hóa phổ biến là dùng ROT13 (dịch mỗi ký tự đi 13 chữ cái).


<img width="1919" height="973" alt="image" src="https://github.com/user-attachments/assets/a15a3709-89b6-4eb2-8d07-b1b040d57a42" />

Bài này tôi sẽ đùng công cụ Burp Site để hỗ trợ. Thật ra không dùng cũng có thể làm nhưng tôi muốn làm nhanh và dễ nhất để mọi người đọc là hiểu ngay.

<img width="1919" height="1021" alt="image" src="https://github.com/user-attachments/assets/a96358ac-a39e-448b-9307-1394a21868b2" />

Tôi vẫn sẽ kiểm tra trong F12 và source code xem có gì đáng ngờ không trước

<img width="714" height="71" alt="image" src="https://github.com/user-attachments/assets/0a26f8b5-c665-44a3-91f1-3539c1fcfce0" />

Theo hint 1 của đề bài: “Một cách mã hóa phổ biến là dùng ROT13 (dịch mỗi ký tự đi 13 chữ cái).” 

Vì vậy, khi nhìn thấy đoạn text trong comment của trang web, mình nghi ngờ nó đã được mã hóa bằng ROT13. Dù chưa chắc chắn, nhưng mình vẫn thử decode.

<img width="1919" height="1029" alt="image" src="https://github.com/user-attachments/assets/3ae7bc22-43a6-42ae-a0d6-0e1cb1656860" />

Kết quả đúng như dự đoán — sau khi áp dụng ROT13, đoạn mã đã được giải ra và cung cấp cho chúng ta một thông tin rất hữu ích.


<img width="1887" height="946" alt="image" src="https://github.com/user-attachments/assets/163f407e-8abc-48ea-9b31-3f5570fd9832" />


Bây giờ chúng ta sẽ quay lại Burp Site đọc request và làm như sau: Proxy --> Intercept on --> open Brower --> Dán link của lab đang giải vào cửa mở vừa mở --> đăng nhập với tên đăng nhập của đề bài ctf-player@picoctf.org và mật khẩu bất kì --> quay lại Burp Site ấn Forward

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/921b5d44-be81-40df-be22-4a8b050f4932" />


Tiếp theo, thêm đoạn " X-Dev-Access: yes" đã giải mã vào trong đoạn code và Foward thêm 1 lần nữa


<img width="1919" height="1018" alt="image" src="https://github.com/user-attachments/assets/0e4fe598-d59a-44d3-8de8-af47398ed5db" />
Flag đã hiện ra và mình đã làm được.
