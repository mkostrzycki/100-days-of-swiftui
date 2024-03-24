```swift
var username: String? = nil

if let unwrappedName = username {
    print("We got a user: \(unwrappedName)")
} else {
    print("The optional was empty.")
}
```

We must alway unwrap optional
```swift
func square(number: Int) -> Int {
    number * number
}

var number: Int? = nil
print(square(number: number)) // ERROR!

// unwrapp
if let unwrappedNumber = number {
    print(square(number: unwrappedNumber))
}

// we can use temporarily variable with the same name - it works only in the scope of `if`
if let number = number {
    print(square(number: number))
}
```
