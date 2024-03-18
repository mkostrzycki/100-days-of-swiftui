```swift
func printTimesTables(number: Int, end: Int) {
    for i in 1...end {
        print("\(i) x \(number) is \(i * number)")
    }
}

printTimesTables(number: 5, end: 20)
```

Return value
```swift
func rollDice() -> Int {
    return Int.random(in: 1...6)
}

let result = rollDice()
print(result)
```

If function have only one line, we can remove `return`
```swift
func rollDice() -> Int {
    Int.random(in: 1...6)
}
```

Return multiple values - tuple
```swift
func getUser() -> (firstName: String, lastName: String) {
    (firstName: "Taylor", lastName: "Swift")
}

let user = getUser()
print("Name: \(user.firstName) \(user.lastName)")
```

We can skip names in returned tuple
```swift
func getUser() -> (firstName: String, lastName: String) {
    ("Taylor", "Swift")
}
```

We can use tuple without named elements
```swift
func getUser() -> (String, String) {
    ("Taylor", "Swift")
}

let user = getUser()
print("Name: \(user.0) \(user.1)")
```

We can decompose returned tuple into variables
```swift
let (firstName, lastName) = getUser()
print("Name: \(firstName) \(lastName)")
```

Or use just one of elements
```swift
let (firstName, _) = getUser()
print("Name: \(firstName)")
```

Remove external parameter name
```swift
func isUppercase(_ string: String) -> Bool {
    string == string.uppercased()
}

let string = "HELLO, WORLD"
let result = isUppercase(string)
```

Or have different external and internal parameter name (argument name is different than parameter name)
```swift
func printTimesTables(for number: Int) {
    for i in 1...12 {
        print("\(i) x \(number) is \(i * number)")
    }
}

printTimesTables(for: 5)
```

