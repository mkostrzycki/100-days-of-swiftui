```swift
var quote = "   The truth is rarely pure and never simple   "
let trimmed = quote.trimmingCharacters(in: .whitespacesAndNewlines)

// instead we can create extension for String type
extension String {
    func trimmed() -> String {
        self.trimmingCharacters(in: .whitespacesAndNewlines)
    }
}

// and use it like this
let trimmed = quote.trimmed()
```

`trimmed()` returns new String. If we want to trim string directly, we can add also `trimm()` method like this
```swift
extension String {
    func trimmed() -> String {
        self.trimmingCharacters(in: .whitespacesAndNewlines)
    }

	mutating func trim() {
	    self = self.trimmed()
	}
}

// and use it like this
var quote = "   The truth is rarely pure and never simple   "
quote.trim()
```

When we return a new value we used `trimmed()`, but when we modified the string directly we used `trim()`. This is intentional, and is part of Swift’s design guidelines: if you’re returning a new value rather than changing it in place, you should use word endings like `ed` or `ing`, like `reversed()`.

**Tip:** Previously I introduced you to the `sorted()` method on arrays. Now you know this rule, you should realize that if you create a variable array you can use `sort()` on it to sort the array in place rather than returning a new copy.

Another useful String extension.
*Important:* Extensions may not add new stored properties, only computed properties.
```swift
extension String {
	var lines: [String] {
	    self.components(separatedBy: .newlines)
	}

    func trimmed() -> String {
        self.trimmingCharacters(in: .whitespacesAndNewlines)
    }

	mutating func trim() {
	    self = self.trimmed()
	}
}

// and we can use it like this
let lyrics = """
But I keep cruising
Can't stop, won't stop moving
It's like I got this music in my mind
Saying it's gonna be alright
"""

print(lyrics.lines.count)
```

We can use extension to our own structs etc.
```swift
struct Book {
    let title: String
    let pageCount: Int
    let readingHours: Int

    init(title: String, pageCount: Int) {
        self.title = title
        self.pageCount = pageCount
        self.readingHours = pageCount / 50
    }
}
```

We can add initializer in extension and then we will have two initializers - default one with all properties and extension one with `title` and `pageCount` only
```swift
struct Book {
    let title: String
    let pageCount: Int
    let readingHours: Int
}

extension Book {
    init(title: String, pageCount: Int) {
        self.title = title
        self.pageCount = pageCount
        self.readingHours = pageCount / 50
    }
}

let lotr = Book(title: "Lord of the Rings", pageCount: 1178, readingHours: 24)

let hobbit = Book(title: "Hobbit", pageCount: 345)
```

