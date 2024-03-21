```swift
class User {
    var name = "Paul"
}

var user = User()
user.name = "Taylor"
user = User()
print(user.name)
```

If we use `let` we will cannot refer to other class instance
```swift
class User {
    var name = "Paul"
}

let user = User()
user.name = "Taylor"
user = User() // ERROR!
print(user.name)
```

Struct vs Class
- Variable classes can have variable properties changed
- Constant classes can have variable properties changed
- Variable structs can have variable properties changed
- Constant structs _cannot_ have variable properties changed

Struct is a value and class is a reference