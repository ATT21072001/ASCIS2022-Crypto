# AES mode CTR ( AES - CTR )



_Một bài AES khá là cơ bản đối với giải lần này :v_





## 1. Giới thiệu
![4e76dd9b-f056-4131-b76b-9c4a1d939636](https://user-images.githubusercontent.com/97930158/196595745-313c8cb6-064a-4867-b32f-7577d1afaf87.png)

* Một challenge khá dễ khi cả 3 team MSEC bên mình đều làm được trong cuộc thi sơ khảo SVATTT vào hôm 15/10/2022 vừa qua. Trước khi vào sâu ta cần hiểu tiêu chuẩn AES là gì.

1. Giới thiệu về AES
AES (Advanced Encryption Standard) là một thuật toán “mã hóa khối” (block cipher). AES trở thành một trong những thuật toán mã hóa phổ biến nhất sử dụng khóa mã đối xứng để mã hóa và giải mã (một số được giữ bí mật dùng cho quy trình mở rộng khóa nhằm tạo ra một tập các khóa vòng).
2. Đặc điểm kỹ thuật
Một số khái niệm:
* Bản rõ (Plaintext): Dạng ban đầu của thông báo
* Bản mã (Ciphertext): Dạng mã của bản rõ ban đầu
* Khóa (Key): thông tin tham số dùng để mã hóa
* Mã hóa (Encryption): Quá trình biến đổi thông tin từ dạng bản rõ sang bản mã bằng khóa hoặc không cần khóa
* Giải mã (Decryption): Quá trình ngược lại biến đổi thông tin từ dạng bản mã sang bản rõ

AES là một thuật toán mã hóa khối đối xứng với độ dài khóa là 128 bít (một chữ số nhị phân có giá trị 0 hoặc 1), 192 bít và 256 bít tương ứng dọi là AES-128, AES-192 và AES-256. AES-128 sử dụng 10 vòng (round), AES-192 sử dụng 12 vòng và AES-256 sử dụng 14 vòng.


AES được thực hiện bởi các hàm theo thứ tự sau: Trộn từng byte (SubBytes), trộn từng hàng (ShiftRows), trộn từng cột (MixColumns) và mã hóa (AddRoundKey). Trong đó SubBytes, ShiftRows, MixColumns có nhiệm vụ làm cho mối quan hệ giữa bản rõ và bản mã bị che khuất (phương thức "mập mờ"). AddRoundKey sử dụng key mã hóa để mã hóa dữ liệu đầu vào bằng việc phân tán những kiểu mẫu của bản rõ sang bản mã (phương thức "khuếch tán")

* Chi tiết thuật toán có thể tham khảo tại: https://vi.wikipedia.org/wiki/Advanced_Encryption_Standard
* Nguồn copy: https://viblo.asia/p/tieu-chuan-ma-hoa-aes-la-gi-va-su-dung-no-trong-ung-dung-ruby-thong-qua-opensslcipher-63vKj0DRl2R
* Cơ chế: 





