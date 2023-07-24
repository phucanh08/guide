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

## Module App

```
├── android
├── ios
├── web
├── app_icon
├── splash
├── lib # Main directory
│   ├── app # MyApp
│   ├── base # Code các base class: BasePageState, BaseBloc
│   ├── config # config khởi tạo application
│   ├── di #  Setup DI cho module app
│   ├── navigation # Khai báo các màn hình và các dialog, bottom sheet được sử dụng trong module app.
│   ├── resource # Khai báo các resources để code UI: Colors, Dimens, generated
│   ├── ui #  UI và Bloc cho từng màn hình.
│   └── main.dart # main file
├── analysis_options.yaml # lint rules
└── pubspec.yaml # pubspec file
```

## Module Domain
## Module Data
## Module Shared
## Module Initializer
## Các folder và file khác