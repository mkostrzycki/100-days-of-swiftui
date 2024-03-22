```swift
let guests = ["Mario", "Luigi", "Peach"]

if guests.isEmpty == false {
    print("Guest count: \(guests.count)")
}
```

We can add extension to `Array`
```swift
extension Array {
    var isNotEmpty: Bool {
        isEmpty == false
    }
}

let guests = ["Mario", "Luigi", "Peach"]

if guests.isNotEmpty == false {
    print("Guest count: \(guests.count)")
}
```

Or even better, we can add extension to Collection protocol and use it in Array, Set, etc
```swift
extension Collection {
    var isNotEmpty: Bool {
        isEmpty == false
    }
}

let guests = ["Mario", "Luigi", "Peach"]

if guests.isNotEmpty == false {
    print("Guest count: \(guests.count)")
}
```

Using protocol extension we can provide default implementation for protocol methods
```swift
protocol Person {
    var name: String { get }
    func sayHello()
}

extension Person {
    func sayHello() {
        print("Hi, I'm \(name)")
    }
}

// now we can create struct without sayHello implementation
struct Employee: Person {
    let name: String
}
```

