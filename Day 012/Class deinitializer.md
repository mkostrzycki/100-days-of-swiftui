```swift
class User {
    let id: Int

    init(id: Int) {
        self.id = id
        print("User \(id): I'm alive!")
    }

    deinit {
        print("User \(id): I'm dead!")
    }
}
```

Each User instance will be deinitialized after each for loop
```swift
for i in 1...3 {
    let user = User(id: i)
    print("User \(user.id): I'm in control!")
}
```

All User instances will be deinitialized after all array elements are removed
```swift
var users = [User]()

for i in 1...3 {
    let user = User(id: i)
    print("User \(user.id): I'm in control!")
    users.append(user)
}

print("Loop is finished!")
users.removeAll()
print("Array is clear!")
```
