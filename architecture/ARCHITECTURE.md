[<- Trở về](../README.md#architecture)

# Kiến trúc

![img](project_architecture.png)

# Cấu trúc thư mục

Chúng ta có tất cả 6 module (package)

* App
* Domain
* Data
* Resources
* Shared
* Initializer

## [Module App](APP.md)
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
│   │   ├── app
│   │   ├── bloc 
│   ├── base
│   ├── common_widgets
│   ├── config
│   ├── di
│   ├── exception_handler
│   ├── navigation
│   ├── resource
│   ├── ui
│   └── main.dart
├── analysis_options.yaml
└── pubspec.yaml
```
## [Module Domain](DOMAIN.md)
## [Module Data](DATA.md)
## [Module Resource](RESOURCE.md)
## [Module Shared](SHARED.md)
## [Module Initializer](INITIALIZER.md)
## Các folder và file khác