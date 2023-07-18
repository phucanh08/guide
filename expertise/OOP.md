[<- Trở về](../README.md)
## Mục lục
- [Bài toán](#bài-toán)
- [OOP là gì?](#oop-là-gì)
    - [Đối tượng (Object)](#đối-tượng-object)
    - [Lớp (Class)](#lớp-class)
- [Tại sao lại nên dùng OOP?](#tại-sao-lại-nên-dùng-oop)
- [4 đặc tính cơ bản của OOP](#4-đặc-tính-cơ-bản-của-oop)
    - [Tính đóng gói (Encapsulation)](#tính-đóng-gói-encapsulation)
    - [Tính kế thừa (Inheritance)](#tính-kế-thừa-inheritance)
    - [Tính đa hình (Polymorphism)](#tính-đa-hình-polymorphism)
    - [Tính trừu tượng (Abstraction)](#tính-trừu-tượng-abstraction)

<br/>

## Bài toán
Đối với các dự án có ít nhất một trong những đặc điểm dưới đây: 

- Lớn và phức tạp.
- Sẽ được tái sử dụng trong nhiều dự án khác nhau.
- Cần có thể mở rộng dễ dàng.
- Cần phải trừu tượng hóa các chi tiết triển khai.

Ta nên sử dụng OOP.
## OOP là gì?
OOP (viết tắt của Object Oriented Programming) – lập trình hướng đối tượng là một phương pháp lập trình dựa trên khái niệm về lớp và đối tượng. OOP tập trung vào các đối tượng thao tác hơn là logic để thao tác chúng.

Mục tiêu của OOP là tối ưu việc quản lý source code, giúp tăng khả năng tái sử dụng và quan trọng hơn hết là giúp tóm gọn các thủ tục đã biết trước tính chất thông qua việc sử dụng các đối tượng.

### Đối tượng (Object)
Đối tượng trong OOP bao gồm 2 thành phần chính:

- Thuộc tính (Attribute): là những thông tin, đặc điểm của đối tượng
- Phương thức (Method): là những hành vi mà đối tượng có thể thực hiện
Để dễ hình dung, ta có một ví dụ thực tế về đối tượng là smartphone. Đối tượng này sẽ có:

Thuộc tính: màu sắc, bộ nhớ, hệ điều hành…
Phương thức: gọi điện, chụp ảnh, nhắn tin, ghi âm…

### Lớp (Class)
Lớp là sự trừu tượng hóa của đối tượng. Những đối tượng có những đặc tính tương tự nhau sẽ được tập hợp thành một lớp. Lớp cũng sẽ bao gồm 2 thông tin là thuộc tính và phương thức.

Một đối tượng sẽ được xem là một thực thể của lớp.

Tiếp nối ví dụ ở phần đối tượng (object) phía trên, ta có lớp (class) smartphone gồm 2 thành phần:

- Thuộc tính: màu sắc, bộ nhớ, hệ điều hành…
- Phương thức: gọi điện, chụp ảnh, nhắn tin, ghi âm…
Các đối tượng của lớp này có thể là: iPhone, Samsung, Oppo, Huawei…

## Tại sao lại nên dùng OOP?

OOP có nhiều lợi thế, bao gồm:

- **Tính mô-đun:** OOP cho phép bạn chia chương trình của mình thành các mô-đun nhỏ, dễ hiểu và dễ bảo trì.
- **Tính tái sử dụng:** Các đối tượng có thể được tái sử dụng trong nhiều chương trình khác nhau.
- **Tính mở rộng:** OOP cho phép bạn dễ dàng thêm các tính năng mới cho chương trình của mình mà không làm ảnh hưởng đến các phần khác của chương trình.
- **Tính trừu tượng:** OOP cho phép bạn tập trung vào các tính năng quan trọng của chương trình của mình mà không cần quan tâm đến chi tiết triển khai.
- **Tính bảo mật:** bảo vệ thông tin thông qua đóng gói.

## 4 đặc tính cơ bản của OOP

### Tính đóng gói (Encapsulation)
Tính đóng gói cho phép che giấu thông tin và những tính chất xử lý bên trong của đối tượng. Các đối tượng khác không thể tác động trực tiếp đến dữ liệu bên trong và làm thay đổi trạng thái của đối tượng mà bắt buộc phải thông qua các phương thức công khai do đối tượng đó cung cấp.

Tính chất này giúp tăng tính bảo mật cho đối tượng và tránh tình trạng dữ liệu bị hư hỏng ngoài ý muốn.

### Tính kế thừa (Inheritance)
Đây là tính chất được sử dụng khá nhiều. Tính kế thừa cho phép xây dựng một lớp mới (lớp Con), kế thừa và tái sử dụng các thuộc tính, phương thức dựa trên lớp cũ (lớp Cha) đã có trước đó. 

Các lớp Con kế thừa toàn bộ thành phần của lớp Cha và không cần phải định nghĩa lại. Lớp Con có thể mở rộng các thành phần kế thừa hoặc bổ sung những thành phần mới.

Ví dụ: 

    - Lớp Cha là smartphone, có các thuộc tính: màu sắc, bộ nhớ, hệ điều hành…
    - Các lớp Con là iPhone, Samsung, Oppo cũng có các thuộc tính: màu sắc, bộ nhớ, hệ điều hành…

### Tính đa hình (Polymorphism)
Tính đa hình trong lập trình OOP cho phép các đối tượng khác nhau thực thi chức năng giống nhau theo những cách khác nhau.

Ví dụ: 

    - Ở lớp smartphone, mỗi một dòng máy đều kế thừa các thành phần của lớp cha nhưng iPhone chạy trên hệ điều hành iOS, còn Samsung lại chạy trên hệ điều hành Android.
    - Chó và mèo cùng nghe mệnh lệnh “kêu đi” từ người chủ. Chó sẽ “gâu gâu” còn mèo lại kêu “meo meo”.

### Tính trừu tượng (Abstraction)
Tính trừu tượng giúp loại bỏ những thứ phức tạp, không cần thiết của đối tượng và chỉ tập trung vào những gì cốt lõi, quan trọng.

Ví dụ: Quản lý nhân viên thì chỉ cần quan tâm đến những thông tin như:

    Họ tên
    Ngày sinh
    Giới tính
    …
Chứ không cần phải quản lý thêm thông tin về:

    Chiều cao
    Cân nặng
    Sở thích
    Màu da
    …
