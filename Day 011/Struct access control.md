```swift
struct BankAccount {
    private var funds = 0

    mutating func deposit(amount: Int) {
        funds += amount
    }

    mutating func withdraw(amount: Int) -> Bool {
        if funds >= amount {
            funds -= amount
            return true
        } else {
            return false
        }
    }
}
```

Swift provides us with several options, but when you’re learning you’ll only need a handful: 
- Use `private` for “don’t let anything outside the struct use this.”
- Use `fileprivate` for “don’t let anything outside the current file use this.”
- Use `public` for “let anyone, anywhere use this.”
- Use `private(set)` for "let anyone read this property, but only let my methods write it."
