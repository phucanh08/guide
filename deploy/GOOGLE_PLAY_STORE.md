[<- Trở về](../README.md)
<div align="center">
  <br/>
  <br/>
  <img alt="logo" height="200" src="https://upload.wikimedia.org/wikipedia/commons/b/bd/Google_Play_logo-2022.png"/>
  <h1>Google Play Store</h1>
</div>


# Mục lục
- [Những thông tin cần chuẩn bị](#những-thông-tin-cần-chuẩn-bị)
- [Bước 1: Đăng ký tài khoản nhà phát triển ứng dụng](#bước-1-đăng-ký-tài-khoản-nhà-phát-triển-ứng-dụng)
- [Bước 2: Tạo ứng dụng](#bước-2-tạo-ứng-dụng)
- [Bước 3: Cài đặt logo và Screenshot cho app](#bước-3-cài-đặt-logo-và-screenshot-cho-app)
- [Bước 4: Tải lên AppBundle](#bước-4-tải-lên-appbundle)
- [Bước 5: Hoàn thành content rating](#bước-5-hoàn-thành-content-rating)
- [Bước 6: Đăng ký giá ứng dụng](#bước-6-đăng-ký-giá-ứng-dụng)


## Những thông tin cần chuẩn bị

Để upload ứng dụng lên App Store trước tiên bạn cần cung cấp đầy đủ thông tin về ứng dụng và submit
lên TestFlight. Các tester của Apple sẽ test ứng dụng để đánh giá có phù hợp với rule để được upload
lên App Store. Nếu được Approve, ứng dụng của bạn sẽ sẵn sàng có mặt trên AS. Ngược lại bạn phải
thay đổi để phù hợp và tiếp tục chờ đợi các vòng tiếp theo. Thông tin cần chuẩn bị:

**Lưu ý:** Đọc kỹ [nội dung xem trước](https://support.google.com/googleplay/android-developer/answer/9866151) của google.
* Tên ứng dụng
* Nội dung giới thiệu
* App Icon
* Đoạn mô tả ngắn (short description)
* Đoạn mô tả chi tiết (full description)
* App Category: Phân loại app của mình bằng việc tìm hiểu thông tin ở [Google Play categories](https://support.google.com/googleplay/android-developer/answer/113475).
* Ảnh chụp màn hình ứng với tấc cả thiết bị hỗ
  trợ ([xem thêm nội dung xem trước](https://support.google.com/googleplay/android-developer/answer/9866151))
* Privacy policy url: Có thể dùng [App Privacy Policy Generator](https://app-privacy-policy-generator.firebaseapp.com/) để tạo.

## Bước 1: Đăng ký tài khoản nhà phát triển ứng dụng

Muốn đăng một ứng dụng lên Google Play, bắt buộc bạn phải có tài khoản Google Developer.

Nếu chưa có thì đăng ký [tại đây](https://play.google.com/apps/publish/signup/).

## Bước 2: Tạo ứng dụng

Sau khi hoàn tất đăng ký, nhấp vào “CREATE APPLICATION”, sau đó chọn dấu “+” để thêm app mới.

Tiếp tục chọn ngôn ngữ mặc định và thêm tiêu đề ứng dụng, sau đó nhấn chọn “CREATE”

Kế đến, điền đầy đủ các thông tin trong phần mô tả ứng dụng, bao gồm: Short description và full
description. Cuối cùng nhấn “SAVE DRAFT.” để kết thúc quá trình điền thông tin cho ứng dụng.

## Bước 3: Cài đặt logo và Screenshot cho app

Bước tiếp theo trong cách upload app lên Google Play là cài đặt logo và screenshot cho ứng dụng của
bạn. Cách thực hiện như sau:

Để tải logo lên, chọn “Add high-res icon”
Để tải ảnh screenshot của ứng dụng, chọn “Add feature graphic.”
Sau khi hoàn thành, nhấn “SAVE DRAFT.” để lưu lại.

Kế đến tại Application type, chọn kiểu Game hoặc app; tại Category, chọn một định dạng cho phù hợp
với ứng dụng của bạn. Đó có thể là Tool, Productivity hoặc Entertainment…

Cuối cùng, đừng quên điền đầy đủ contact detail và thêm liên kết chính sách bảo mật.

## Bước 4: Tải lên AppBundle

Đầu tiên, chọn tab “app release” và chọn “CREATE RELEASE”. Tiếp theo nhấp vào “Opt-out” (trong
trường hợp nhà phát triển đã tạo APK với signkey) và chọn “browse files” và bắt đầu tải file APK
lên.

## Bước 5: Hoàn thành content rating

Đến đây, chúng ta đã hoàn thành 80% các bước trong cách đưa app lên Google Play rồi. Ở phần này,
người phát triển ứng dụng chỉ cần trả lời đầy đủ các câu hỏi do Google đưa ra. Chủ yếu xoay quanh
các vấn đề như ứng dụng có liên quan đến vấn đề nhạy cảm, phản động hay không, phù hợp cho lứa tuổi
và giới tính nào… Cứ trả lời đúng và đủ là được.

## Bước 6: Đăng ký giá ứng dụng

Ở phần này bạn có hai lựa chọn: trả phí hoặc miễn phí. Tuy nhiên, hãy lưu ý rằng, một khi đã chọn
miễn phí, bạn sẽ không thể thay đổi quyết định về sau này. Do đó hãy cân nhắc thật kỹ.

Nếu đăng ký là ứng dụng trả phí, người phát triển ứng dụng phải cài đặt phương thức thanh toán để
nhận tiền từ Google khi có người mua ứng dụng của bạn.

Sau khi hoàn thành tất cả các bước, chọn lại “App Release” và nhấn vào “Start Rollout to
Production”, chọn “Confirm”.

Cách đăng tải app lên Google Play chỉ đơn giản thế thôi, việc còn lại hãy thư giãn và chờ Google
đánh giá cũng như chấp thuận là ứng dụng có thể được công khai trên Google Play rồi. Thông thường,
quá trình này sẽ mất khoảng 4 – 6 tiếng.