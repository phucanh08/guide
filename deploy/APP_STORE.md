[<- Trở về](../README.md)
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
- [Bước 4: Archive App trên Xcode](#bước-4-archive-app-trên-xcode)
- [Bước 5: Tạo Version Release](#bước-5-tạo-version-release)

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
2. Trang Ứng dụng của tôi trống cho đến khi bạn tạo bản ghi ứng dụng đầu tiên của mình.
Từ menu bật lên, chọn Ứng dụng mới.
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

## Bước 4: Archive App trên Xcode

[Tham khảo](https://developer.apple.com/documentation/xcode/distributing-your-app-for-beta-testing-and-releases)

## Bước 6: Tạo Version Release