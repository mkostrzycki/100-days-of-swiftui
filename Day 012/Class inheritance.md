```swift
class Employee {
    let hours: Int

    init(hours: Int) {
        self.hours = hours
    }

	func printSummary() {
	    print("I work \(hours) hours a day.")
	}
}

class Developer: Employee {
    func work() {
        print("I'm writing code for \(hours) hours.")
    }
}

class Manager: Employee {
    func work() {
        print("I'm going to meetings for \(hours) hours.")
    }
}
```

This is where Swift enforces a simple rule: if a child class wants to change a method from a parent class, you must use `override` in the child class’s version. This does two things:
1. If you attempt to change a method without using `override`, Swift will refuse to build your code. This stops you accidentally overriding a method.
2. If you use `override` but your method doesn’t actually override something from the parent class, Swift will refuse to build your code because you probably made a mistake.

```swift
class Developer: Employee {
    func work() {
        print("I'm writing code for \(hours) hours.")
    }

	override func printSummary() {
    print("I'm a developer who will sometimes work \(hours) hours a day, but other times spend hours arguing about whether code should be indented using tabs or spaces.")
	}
}
```

**Tip:** If you know for sure that your class should not support inheritance, you can mark it as `final`. This means the class itself can inherit from other things, but can’t be used to inherit _from_ – no child class can use a final class as its parent.

```swift
final class Developer: Employee {
    func work() {
        print("I'm writing code for \(hours) hours.")
    }
}

final class Manager: Employee {
    func work() {
        print("I'm going to meetings for \(hours) hours.")
    }
}
```

