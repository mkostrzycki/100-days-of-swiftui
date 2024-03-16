Create integer type const/variable
```swift
let score = 10
```

Use `_` as thousands separator.
```swift
let reallyBig = 100_000_000
```
It's for readability. Swift will ignore all `_`
```swift
let reallyBig = 1_00__00___00____00
```

### compound assignment operators
```swift
var counter = 10
counter += 5
counter *= 2
counter -= 10
counter /= 2
```

### is int multiple of other int?
```swift
let number = 120
print(number.isMultiple(of: 3))
//or shorter
print(120.isMultiple(of: 3))
```
