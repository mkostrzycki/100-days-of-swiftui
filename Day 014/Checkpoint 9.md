Write a function that accepts an optional array of integers, and returns one randomly. If the array is missing or empty, return a random number in the range 1 through 100.
Write your function in a single line of code.

```swift
func randomInt(from ints: [Int]?) -> Int { ints?.randomElement() ?? Int.random(in: 1...100) }

print(randomInt(from: nil))
print(randomInt(from: Array<Int>()))
print(randomInt(from: [8, 23, 34]))
```

