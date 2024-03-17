This time the challenge is to create an array of strings, then write some code that prints the number of items in the array and also the number of _unique_ items in the array.

```swift
let strings = ["One", "Two", "Three", "Two", "Four"]
print("There is \(strings.count) elements in the array.") // 5

// create Set from Array
let uniqueStrings = Set(strings)
print("There is \(uniqueStrings.count) unique elements in the array.") // 4
```

