You can copy struct and then you will have independent instance of struct, but you can't copy class in the same way. If you want to copy class, you must provide method for that.

```swift
class User {
    var username = "Anonymous"

    func copy() -> User {
        let user = User()
        user.username = username
        return user
    }
}
```

Struct is a value and class is a reference
