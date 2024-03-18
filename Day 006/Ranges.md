### Closed range operator going from a…b
```swift
let range: ClosedRange = 0...10
print(range.first!) // 0
print(range.last!) // 10
```

```swift
let names = ["Antoine", "Maaike", "Jaap"]
let range: CountableClosedRange = 0...2
print(names[range]) // ["Antoine", "Maaike", "Jaap"]
```

```swift
let names = ["Antoine", "Maaike", "Jaap"]
print(names[0...2]) // ["Antoine", "Maaike", "Jaap"]
```

### Half-open range operator going from a..\<b
```swift
let range: Range = 0..<10
print(range.first!) // 0
print(range.last!) // 9
```

```swift
let names = ["Antoine", "Maaike", "Jaap"]
print(names[0..<names.count]) // ["Antoine", "Maaike", "Jaap"]
```

### One-sided operator going from a…
```swift
let names = ["Antoine", "Maaike", "Jaap"]
print(names[...2]) // ["Antoine", "Maaike", "Jaap"]
```

```swift
let names = ["Antoine", "Maaike", "Jaap"]
print(names[1...]) // ["Maaike", "Jaap"]
```

