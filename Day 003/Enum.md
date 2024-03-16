```swift
enum Weekday {
    case monday
    case tuesday
    case wednesday
    case thursday
    case friday
}
```

```swift
enum Weekday {
    case monday, tuesday, wednesday, thursday, friday
}
```

Use enum values
```swift
var day = Weekday.monday
day = Weekday.tuesday
day = Weekday.friday
```

After assigned value to variable we can skip enum name
```swift
var day = Weekday.monday
day = .tuesday
day = .friday
```
