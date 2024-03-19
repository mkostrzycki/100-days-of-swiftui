Pass closure to another function (similar to anonymous functions from PHP)
```swift
let captainFirstTeam = team.sorted(by: { (name1: String, name2: String) -> Bool in
    if name1 == "Suzanne" {
        return true
    } else if name2 == "Suzanne" {
        return false
    }

    return name1 < name2
})
```

Parameters in clousure
```swift
// function
func pay(user: String, amount: Int) {
    // code
}

// closure
let payment = { (user: String, amount: Int) in
    // code
}
```

We don't use parameter names when calling closure
```swift
let payment = { (user: String, amount: Int) in
    // code
}

payment("Adam", 10)
```

Closure cannot have external parameter name
```swift
let payment = { (for user: String) in // ERROR!
    // code
}
```
