[<- Trở về](../README.md#conventions)

# Naming Conventions

### Mục lục
- [Event Conventions](#event-conventions)
- [State Conventions](#state-conventions)

<br/>
<br/>

# Event Conventions
Các sự kiện nên được đặt tên ở thì quá khứ vì các sự kiện là những thứ đã xảy ra từ quan điểm của khối.

`BlocSubject` + `Noun (optional)` + ` Verb (event)`


### Ví dụ

### ✅ Good

```dart

@freezed
class CounterEvent with _$CounterEvent {
  const factory CounterEvent.started() = _CounterStarted;
  const factory CounterEvent.incrementPressed() = _CounterIncrementPressed;
  const factory CounterEvent.decrementPressed() = _CounterDecrementPressed;
  const factory CounterEvent.incrementRetried() = _CounterIncrementRetried;
}

```


### ❌ Bad

```dart

@freezed
class CounterEvent with _$CounterEvent {
  const factory CounterEvent.start() = _Start;
  const factory CounterEvent.increase() = _Increase;
  const factory CounterEvent.decreaseCounter() = _DecreaseCounter;
  const factory CounterEvent.incrementRetried() = _IncrementRetried;
}

```

# State Conventions

Các trạng thái phải là danh từ vì trạng thái chỉ là ảnh chụp nhanh tại một thời điểm cụ thể. Có hai cách phổ biến để biểu diễn trạng thái: sử dụng các lớp con hoặc sử dụng một lớp duy nhất.

### Các lớp con

`BlocSubject` + `Verb (action)` + `State`

> Khi biểu diễn trạng thái dưới dạng các lớp con `State` phải là một trong các trạng thái sau: `Initial` | `Success` | `Failure` | `InProgress` và các trạng thái ban đầu phải tuân theo quy ước: BlocSubject + Initial.

### Lớp đơn

`BlocSubject` + `State`

> Khi biểu diễn trạng thái dưới dạng một lớp cơ sở duy nhất, nên sử dụng enum có tên `BlocSubject` + `Status` để biểu thị trạng thái của trạng thái: `success` | `success` | `failure` | `loading`.

Lớp trạng thái cơ sở phải luôn được đặt tên: `BlocSubject` + `State`.

### **Ví dụ**

###  ✅ Good

#### Các lớp con

```dart

@freezed
class CounterState with _$CounterState {
  const factory CounterState.initial() = _CounterInitial;
  const factory CounterState.loadInProgress() = _CounterLoadInProgress;
  const factory CounterState.loadSuccess() = _CounterLoadSuccess;
  const factory CounterState.loadFailure() = _CounterLoadFailure;
}

```

#### Lớp đơn

```dart

enum CounterStatus { initial, loading, success, failure }

@freezed
class CounterState with _$CounterState {
  const factory CounterState({@Default(CounterStatus.initial) CounterStatus status}) = _CounterState;
}

```


### ❌ Bad

```dart
@freezed
class CounterEvent with _$CounterEvent {
  const factory CounterEvent.initial() = _Initial ;
  const factory CounterEvent.loading() = _Loading;
  const factory CounterEvent.success() = _Success;
  const factory CounterEvent.succeeded() = _Succeeded;
  const factory CounterEvent.loaded() = _Loaded;
  const factory CounterEvent.failure() = _Failure;
  const factory CounterEvent.failed() = _Failed;
}
```

<style>
code {
  color: #d22778;
  font-weight: bold;
  background-color: #0e2233;
  border-radius: 2px;
  padding: 2px 5px;
  margin: 0 2px;
}
</style>