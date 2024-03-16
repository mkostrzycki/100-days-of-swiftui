```swift
let firstPart = "Hello, "
let secondPart = "world!"
let greeting = firstPart + secondPart
```

### string interpolation
```swift
let name = "Taylor"
let age = 26
let message = "Hello, my name is \(name) and I'm \(age) years old."
print(message) // Hello, my name is Taylor and I'm 26 years old.
```

String interpolation is much more efficient than using `+` to join strings one by one, but there’s another important benefit too: you can pull in integers, decimals, and more with no extra work.

You can do some calculations inside string interpolation
```swift
print("5 x 5 is \(5 * 5)")
```
