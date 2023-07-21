[<- Trở về](../README.md#hướng-dẫn-deploy-app)
<div align="center">
  <br/>
  <br/>
  <img alt="logo" height="200" src="https://upload.wikimedia.org/wikipedia/commons/2/27/App_Store_macOS.png"/>
  <h1>App Store</h1> 
</div>

[Tham khảo](https://developer.apple.com/help/app-store-connect/create-an-app-record/add-a-new-app/)

## Mục lục
- [Những thông tin cần chuẩn bị](#những-thông-tin-cần-chuẩn-bị)
- [Bước 1: Đăng kí tham gia Apple Developer](#bước-1-đăng-kí-tham-gia-apple-developer)
- [Bước 2: Tạo Bundle Id](#bước-2-tạo-bundle-id)
- [Bước 3: Tạo App trên App Store Connect](#bước-3-tạo-app-trên-app-store-connect)
- [Bước 4: Phân phối ứng dụng của bạn để thử nghiệm và phát hành beta](#bước-4-phân-phối-ứng-dụng-của-bạn-để-thử-nghiệm-và-phát-hành-beta)
  - [Tổng quan](#tổng-quan)
  - [Tạo kho lưu trữ ứng dụng của bạn](#tạo-kho-lưu-trữ-ứng-dụng-của-bạn)
  - [Tạo phân phối tùy chỉnh](#tạo-phân-phối-tùy-chỉnh)
  - [Phân phối phiên bản beta](#phân-phối-phiên-bản-beta)

## Những thông tin cần chuẩn bị

Để upload ứng dụng lên App Store trước tiên bạn cần cung cấp đầy đủ thông tin về ứng dụng và submit
lên TestFlight. Các tester của Apple sẽ test ứng dụng để đánh giá có phù hợp với rule để được upload
lên App Store. Nếu được Approve, ứng dụng của bạn sẽ sẵn sàng có mặt trên AS. Ngược lại bạn phải
thay đổi để phù hợp và tiếp tục chờ đợi các vòng tiếp theo. Thông tin cần chuẩn bị:

* Tên ứng dụng
* Nội dung giới thiệu
* App Icon (1024 x 1024)
* Ảnh chụp màn hình ứng với tấc cả thiết bị hỗ
  trợ ([thông tin về kích thước màn hình](https://help.apple.com/app-store-connect/#/devd274dd925))

## Bước 1: Đăng kí tham gia Apple Developer

Để đẩy ứng dụng lên app store ta cần có tài khoản Apple Developer nếu chưa có thì hãy request đăng ký hoặc nhờ add vào dự án.

## Bước 2: Tạo Bundle Id

1. Trong [Certificates, Identifiers & Profiles](https://developer.apple.com/account/resources), bấm vào Số nhận dạng trong thanh bên, sau đó bấm vào nút thêm (+) ở trên cùng bên trái.
Chọn ID ứng dụng từ danh sách tùy chọn và nhấp vào tiếp tục.
2. Từ các tùy chọn, xác nhận loại ID ứng dụng được chọn tự động, sau đó nhấp vào Tiếp tục.
Nhập tên hoặc mô tả cho ID ứng dụng trong trường Mô tả.
3. Để tạo ID ứng dụng rõ ràng, hãy chọn ID ứng dụng rõ ràng và nhập ID gói của ứng dụng vào trường ID gói.
4. ID ứng dụng rõ ràng mà bạn nhập vào đây phải khớp với ID gói bạn đã nhập trong ngăn Tóm tắt của mục tiêu trong Xcode.
5. Để tạo ID ứng dụng ký tự đại diện, hãy chọn ID ứng dụng ký tự đại diện và nhập hậu tố ID gói vào trường ID gói.
6. Chọn các hộp kiểm tương ứng để bật các khả năng của ứng dụng mà bạn muốn sử dụng.
7. Các khả năng có sẵn cho loại ứng dụng và tư cách thành viên chương trình của bạn xuất hiện trong Khả năng. Hộp kiểm bị tắt nếu công nghệ yêu cầu ID ứng dụng rõ ràng và bạn đang tạo ID ứng dụng ký tự đại diện hoặc công nghệ được bật theo mặc định. Không phải tất cả các khả năng đều đủ điều kiện cho tất cả các nền tảng.
8. Bấm Tiếp tục, sau đó xem lại thông tin đăng ký, rồi bấm Đăng ký.

## Bước 3: Tạo App trên App Store Connect

1. Từ Ứng dụng của tôi, nhấp vào nút thêm (+) ở trên cùng bên trái.

2. Trang Ứng dụng của tôi trống cho đến khi bạn tạo bản ghi ứng dụng đầu tiên của mình. Từ menu bật lên, chọn Ứng dụng mới.

3. Trong hộp thoại Ứng dụng mới, hãy chọn một hoặc nhiều nền tảng và nhập thông tin ứng dụng.
Nếu bạn đã đăng ký với tư cách là một công ty, bạn sẽ có tùy chọn [đặt tên nhà phát triển của mình](https://developer.apple.com/help/app-store-connect/create-an-app-record/set-your-developer-name-on-the-app-store).


        Lưu ý: Các ứng dụng chỉ dành cho đồng hồ được coi là một phần của nền tảng iOS trong App Store Connect.

![image](https://developer.apple.com/help/app-store-connect/create-an-app-record/add-a-new-app/images/manage-apps-add-new-4_2x.png)

4. Trong Quyền truy cập của người dùng, hãy chọn Quyền truy cập có giới hạn hoặc Quyền truy cập đầy đủ. Nếu bạn chọn Quyền truy cập có giới hạn, hãy chọn những người dùng mà bạn muốn truy cập vào ứng dụng này.

    **Truy cập Báo cáo**

        Vai trò Truy cập vào Báo cáo là một vai trò bổ sung chỉ có thể được thêm cho người dùng có vai trò Người quản lý ứng dụng, Nhà phát triển, Tiếp thị hoặc Bán hàng. Những người dùng này có thể tải xuống các báo cáo được liên kết với vai trò của họ. Nếu vai trò Truy cập Báo cáo được thêm vào, thì người dùng có quyền truy cập vào tất cả các ứng dụng. Theo mặc định, người dùng Quản trị viên và Tài chính có vai trò Truy cập vào Báo cáo.

5. Người dùng có vai trò Chủ tài khoản, Quản trị viên, Tài chính và Quyền truy cập vào Báo cáo có thể xem tất cả các ứng dụng vì những vai trò đó không thể giới hạn quyền truy cập ứng dụng của họ.
Nhấp vào Tạo và tìm thông báo cho biết thông tin bị thiếu.

Sau khi bạn tạo bản ghi Kết nối App Store cho một ứng dụng, ứng dụng đó sẽ xuất hiện trong Ứng dụng của tôi và [trạng thái ứng dụng](https://developer.apple.com/help/app-store-connect/reference/app-and-submission-statuses) là Chuẩn bị gửi. Bạn có thể chọn ứng dụng trên trang này để [xem và chỉnh sửa thông tin ứng dụng](https://developer.apple.com/help/app-store-connect/create-an-app-record/view-and-edit-app-information).

## Bước 4: Phân phối ứng dụng của bạn để thử nghiệm và phát hành beta

### Tổng quan
Sau khi bạn kiểm tra kỹ lưỡng ứng dụng của mình trong Xcode, hãy phân phối ứng dụng đó cho những người thử nghiệm bản beta hoặc phát hành ứng dụng đó cho người dùng để chạy trên thiết bị cá nhân của họ. Chọn phương thức phân phối dựa trên nền tảng và giai đoạn phát triển của ứng dụng cũng như việc bạn có tham gia Chương trình dành cho nhà phát triển của Apple hay không. Trước khi bạn phát hành ứng dụng của mình cho người dùng, hãy phân phối bản dựng cuối cùng của bạn bằng một trong các phương pháp thử nghiệm beta.

Hãy đọc kỹ [Chuẩn bị ứng dụng của bạn để phân phối](https://developer.apple.com/documentation/xcode/preparing-your-app-for-distribution) để hoàn tất cấu hình dự án của bạn, trước khi thực hiện tiếp các bước tiếp theo.

### Tạo kho lưu trữ ứng dụng của bạn
[tham khảo](https://developer.apple.com/documentation/xcode/distributing-your-app-for-beta-testing-and-releases#Create-an-archive-of-your-app)

Để sử dụng bất kỳ phương thức phân phối nào, trước tiên hãy tạo một kho lưu trữ ứng dụng của bạn. Kho lưu trữ là bản dựng ứng dụng của bạn, bao gồm thông tin gỡ lỗi, mà Xcode lưu trữ trong một gói. Xcode đóng gói lại nội dung của kho lưu trữ dựa trên cấu hình phân phối mà bạn chọn cho bản phân phối của mình.

Trong cửa sổ chính của dự án Xcode của bạn, hãy chọn một lược đồ và đích chạy để xây dựng từ menu thanh công cụ Lược đồ. Sau đó, chọn Sản phẩm > Lưu trữ để tạo các mục tiêu có trong sơ đồ đó, cho loại thiết bị bạn chọn và tạo một kho lưu trữ xuất hiện trong trình tổ chức Lưu trữ.

![image_2](https://docs-assets.developer.apple.com/published/197cc74857f2b024622234a622112069/distributing-your-app-for-beta-testing-and-releases-1~dark@2x.png)

Bạn có thể mở trực tiếp trình tổ chức Lưu trữ bằng cách chọn Cửa sổ > Trình tổ chức. Nếu bạn muốn xác nhận rằng ứng dụng của mình đã sẵn sàng để gửi tới TestFlight hoặc App Store mà chưa gửi ứng dụng đó, hãy chọn kho lưu trữ của bạn rồi nhấp vào Xác thực ứng dụng. Xcode sẽ thực hiện xác thực ban đầu có giới hạn, tự động cho ứng dụng và cung cấp phản hồi.

Đối với ứng dụng Mac được xây dựng bằng Mac Catalyst, hãy tạo các kho lưu trữ riêng cho phiên bản iPad và Mac. Khi tạo kho lưu trữ cho phiên bản Mac, hãy chọn My Mac làm đích chạy.

### Tạo phân phối tùy chỉnh 

[Tham khảo](https://developer.apple.com/documentation/xcode/distributing-your-app-for-beta-testing-and-releases#Create-a-custom-distribution)

Chọn đúng file, version rồi chọn Distribute App

![img](https://docs-assets.developer.apple.com/published/77363ce6c110e17609a4d6f829385664/distributing-your-app-for-beta-testing-and-releases-3~dark@2x.png)

Chọn từ các phương thức phân phối sau:

**App Store Connect**

Phân phối bằng TestFlight hoặc thông qua App Store.

**Ad Hoc**

Phân phối cho một số thiết bị hạn chế mà bạn đăng ký trong App Store Connect. Để biết thêm thông tin về cách phân phối tới các thiết bị bạn đăng ký, hãy xem [Phân phối ứng dụng của bạn tới các thiết bị đã đăng ký](https://developer.apple.com/documentation/xcode/distributing-your-app-to-registered-devices).

**Enterprise**

Phân phối cho các thành viên trong tổ chức của bạn nếu bạn là một phần của [Chương trình doanh nghiệp dành cho nhà phát triển của Apple](https://developer.apple.com/programs/enterprise) và sẵn sàng phát hành ứng dụng của bạn cho người dùng trong tổ chức của bạn.

**Development**

Phân phối cho một số thiết bị hạn chế mà bạn đăng ký trong App Store Connect. Để biết thêm thông tin về cách phân phối tới các thiết bị bạn đăng ký, hãy xem [Phân phối ứng dụng của bạn tới các thiết bị đã đăng ký](https://developer.apple.com/documentation/xcode/distributing-your-app-to-registered-devices).

**Copy App**

Phân phối ứng dụng macOS mà không cần ký mã. Phương thức phân phối này chỉ khả dụng cho các ứng dụng được tạo cho Mac.

Nếu bạn chọn Kết nối App Store hoặc ID nhà phát triển làm phương thức phân phối của mình, thì bạn cũng chọn một tùy chọn đích. Bạn có thể chọn tải bản dựng của mình lên App Store hoặc Xuất bản dựng của bạn cục bộ để tải lên sau.

![img](https://docs-assets.developer.apple.com/published/321015057cff44ee06de6dfd0aabc04d/distributing-your-app-for-beta-testing-and-releases-4~dark@2x.png)

Khi phân phối ứng dụng của bạn trên TestFlight hoặc App Store, hãy chọn cách quản lý biểu tượng và số bản dựng:

![img](https://docs-assets.developer.apple.com/published/cb1a64848358cc290d3078049c05c7fa/distributing-your-app-for-beta-testing-and-releases-5~dark@2x.png)

**Strip Swift symbols**

Giảm kích thước ứng dụng của bạn bằng cách loại bỏ các biểu tượng khỏi thư viện tiêu chuẩn Swift. Cài đặt này chỉ khả dụng nếu dự án của bạn có nhúng các thư viện Swift.

**Upload your app’s symbols**

Cho phép Apple cung cấp cho bạn nhật ký sự cố được tượng trưng và thông tin chẩn đoán khác. Nhật ký được tượng trưng thay thế địa chỉ bộ nhớ trong nhật ký bằng tên hàm và số dòng có thể đọc được của con người. Các biểu tượng cũng có thể hữu ích trong việc kiểm tra tính tương thích của ứng dụng của bạn với các sản phẩm và dịch vụ của Apple.

**Manage version and build number**

Quản lý phiên bản và số bản dựng

**TestFlight internal testing only**

Chuẩn bị ứng dụng để phân phối thông qua TestFlight và hạn chế quyền truy cập vào nhóm của bạn. Sử dụng tùy chọn này để ngăn không cho bản dựng phát triển của ứng dụng của bạn được gửi tới App Store.

Khi chọn một phương pháp phân phối liên quan đến ký mã, hãy chọn 
“Automatically manage signing” để Xcode quản lý việc ký.

![img](https://docs-assets.developer.apple.com/published/52f058810745ad89509da776d371f0ec/distributing-your-app-for-beta-testing-and-releases-6~dark@2x.png)

### Phân phối phiên bản beta

[Tham khảo](https://developer.apple.com/documentation/xcode/distributing-your-app-for-beta-testing-and-releases#Distribute-a-beta-version)

Sau khi thử nghiệm phiên bản beta bản dựng cuối cùng của bạn, hãy gửi bản dựng đó cho Đánh giá ứng dụng, sau đó cung cấp bản dựng đó trên App Store. Để biết thêm thông tin về quy trình xuất bản, hãy xem [Tổng quan về xuất bản ứng dụng](https://developer.apple.com/help/app-store-connect/manage-your-apps-availability/overview-of-publishing-your-app).

Truy cập [Đánh giá ứng dụng](https://developer.apple.com/app-store/review/) để xem lại Nguyên tắc giao diện con người và cửa hàng ứng dụng. Đối với ứng dụng watchOS, hãy đọc [Chuẩn bị ứng dụng watchOS của bạn để gửi](https://developer.apple.com/app-store/watch).

Bạn có thể cần nhập thông tin bổ sung trong App Store Connect trước khi có thể gửi ứng dụng của mình để Xét duyệt ứng dụng. Sau khi ứng dụng của bạn được tải lên hoặc phát hành, bạn không thể thay đổi một số siêu dữ liệu này, vì vậy, điều quan trọng là bạn phải chọn cài đặt của mình một cách cẩn thận. Để biết thêm thông tin về siêu dữ liệu này, hãy chuyển đến [Required, localizable, and editable properties](https://developer.apple.com/help/app-store-connect/reference/required-localizable-and-editable-properties) trong Trợ giúp kết nối App Store.

Nếu bạn đã sử dụng TestFlight để phân phối phiên bản beta và đã nhập thông tin bổ sung mà App Store yêu cầu để phát hành, chỉ cần gửi bản dựng cuối cùng xuất hiện trong App Store Connect để Đánh giá ứng dụng.

Nếu bạn không phân phối bản dựng cuối cùng bằng TestFlight, hãy chuẩn bị ứng dụng của bạn để phân phối và tạo kho lưu trữ ứng dụng của bạn. Xác thực kho lưu trữ và sửa bất kỳ lỗi xác thực nào trước khi tiếp tục. Sau đó, tải nó lên App Store Connect và đợi nó vượt qua các bài kiểm tra xác thực của App Store Connect.

Để gửi bản dựng cho Xét duyệt ứng dụng, hãy chuyển đến [Gửi để xem xét](https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-for-review).
