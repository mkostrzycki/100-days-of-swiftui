Parameter default value
```swift
func printTimesTables(for number: Int, end: Int = 12) {
    for i in 1...end {
        print("\(i) x \(number) is \(i * number)")
    }
}

printTimesTables(for: 5, end: 20)
printTimesTables(for: 8)
```

### Throw errors
Define possible `Error` type enum
```swift
enum PasswordError: Error {
    case short, obvious
}
```

Declare that function can throw errors
```swift
func checkPassword(_ password: String) throws -> String {
...
```

Throw errors in function body
```swift
func checkPassword(_ password: String) throws -> String {
    if password.count < 5 {
        throw PasswordError.short
    }

    if password == "12345" {
        throw PasswordError.obvious
    }
...
```

### try-catch
```swift
do {
    try someRiskyWork()
} catch {
    print("Handle errors here")
}
```

```swift
let string = "12345"

do {
    let result = try checkPassword(string)
    print("Password rating: \(result)")
} catch PasswordError.short {
    print("Please use a longer password.")
} catch PasswordError.obvious {
    print("I have the same combination on my luggage!")
} catch {
    print("There was an error.")
    // print(error)
    print(error.localizedDescription)
}
```

