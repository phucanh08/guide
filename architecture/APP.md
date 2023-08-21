[<- Trở về](ARCHITECTURE.md#module-app)

# Module App
Chúng ta sẽ code UI và Bloc trong module này. Đây cũng là nơi được khai báo hàm main() là entry point để run app của chúng ta.

Hai folder app_icon và splash chứa hai file app-icon.yaml và splash.yaml để chúng ta config app icon và màn hình splash của project theo hướng dẫn của thư viện flutter_launcher_icons và flutter_native_splash.

```
├── android
├── ios
├── web
├── app_icon
├── splash
├── lib
│   ├── app 
│   │   ├── app.dart
│   │   ├── bloc 
│   ├── base
│   ├── common_widgets
│   ├── config
│   ├── di
│   ├── exception_handler
│   ├── navigation
│   ├── resource
│   ├── ui
│   ├── app.dart
│   └── main.dart
├── analysis_options.yaml
└── pubspec.yaml
```
## 1. Folder `android`

    Nơi chứa các config để build android

## 2. Folder `ios`

    Nơi chứa các config để build ios

## 3. Folder `web`

    Nơi chứa các config để build web

## 4. Folder `app_icon`

    Nơi chứa file `app-icon.yaml` để chúng ta config app icon theo hướng dẫn của thư viện [flutter_launcher_icons](https://pub.dev/packages/flutter_launcher_icons)

## 5. Folder `splash`

    Nơi chứa file `splash.yaml` để chúng ta config app icon theo hướng dẫn của thư viện [flutter_native_splash](https://pub.dev/packages/flutter_native_splash)

## 6. Folder `lib`

### 6.1. Folder `app` 
#### 6.1.1 File `app.dart`
    File này là nơi chúng ta khởi tạo widget gốc của ứng dụng.
#### 6.1.2 Folder `bloc`
    Folder này là nơi chúng ta khởi tạo bloc tổng cho toàn bộ dự án. Bloc này sẽ được dùng chung cho tất cả màn hình. Ví dụ các task như đổi ngôn ngữ, switch từ dark mode sang light mode cần update UI của tất cả màn hình thì bạn nên dùng đến AppBloc.
### 6.2. Folder `base` 
    Folder này là nơi code các base class như BasePageState, BaseBloc, BaseEvent và BaseState...
### 6.3. Folder `common_widgets` 
    Folder này là nơi mình code các UI dùng chung cho nhiều màn hình và quan trọng là nó có thể dùng đi dùng lại cho nhiều dự án. Ví dụ common_dialog, common_app_bar, common_scaffold,… thì mỗi dự án khác nhau, ta chỉ cần vào thay đổi một chút về style cho phù hợp với dự án đó là có thể dùng được.
### 6.4. Folder `config` 
    Folder này là nơi để mình gọi các hàm config cho module app như Firebase.initializeApp(),…
### 6.5. Folder `di` 
    Folder này là nơi setup DI cho module app
### 6.6. Folder `exception_hanler` 
    Folder này là nơi tập trung xử lý tất cả lỗi có thể xảy ra trong toàn project.
### 6.7. Folder `navigation` 
    Folder này là nơi khai báo các màn hình và các dialog, bottom sheet được sử dụng trong app.
### 6.8. Folder `ui` 
```
Folder này là nơi mình code UI và Bloc cho từng màn hình.

Cấu trúc thư mục trong folder:
├── ui
│   ├── features
│   │   ├── bloc
│   │   ├── widgets
│   │   ├── feature1 
│   │   ├── feature2
│   ├── feature3
│   │   ├── feature3_screen.dart
│   │   ├── widgets
│   │   ├── bloc 
│   ├── widgets
│   │   ├── dialog
│   │   │   ├── dialog1.dart
│   │   │   ├── dialog2.dart
│   │   │   ├── dialog.dart
│   │   ├── widget2.dart
│   │   ├── widgets.dart
└── └── ui.dart
```
### 6.9. File `app.dart` 
    File này là file chứa mục lục cho toàn bộ folder lib.
### 6.10. File `main.dart` 
    File này là file chứa hàm main (hàm khởi tạo của ứng dụng).
## 7. File `pubspec.yaml`
    Thư mục này là nơi định nghĩa các thông tin về dự án của mình, bao gồm tên, phiên bản, các phụ thuộc, các tài liệu tài nguyên, cài đặt plugin và nhiều thứ khác.
