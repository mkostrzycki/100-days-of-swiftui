```swift
if someCondition {
    print("Do something")
}
```

```swift
let speed = 88
let percentage = 85
let age = 18

if speed >= 88 {
    print("Where we're going we don't need roads.")
}

if percentage < 85 {
    print("Sorry, you failed the test.")
}

if age >= 18 {
    print("You're eligible to vote")
}
```

We can compare also strings
```swift
let ourName = "Dave Lister"
let friendName = "Arnold Rimmer"

if ourName < friendName {
    print("It's \(ourName) vs \(friendName)")
}

if ourName > friendName {
    print("It's \(friendName) vs \(ourName)")
}
```


```swift
let country = "Canada"

if country == "Australia" {
    print("G'day!")
}

let name = "Taylor Swift"

if name != "Anonymous" {
    print("Welcome, \(name)")
}
```

Check if string is empty
```swift
// Create the username variable
var username = "taylorswift13"

// If `username` contains an empty string
if username == "" {
    // Make it equal to "Anonymous"
    username = "Anonymous"
}

// Now print a welcome message
print("Welcome, \(username)!")
```

Do not count string for checking if it is empty - this is not efficient in Swift
```swift
if username.count == 0 {
    username = "Anonymous"
}
```

We can (should) use `isEmpty` on strings, arrays, dictionaries and sets
```swift
if username.isEmpty == true {
    username = "Anonymous"
}
```

### compare enum values
```swift
enum Sizes: Comparable {
    case small
    case medium
    case large
}

let first = Sizes.small
let second = Sizes.large
print(first < second) // true
```
`small` comes before `large` in the enum case list.