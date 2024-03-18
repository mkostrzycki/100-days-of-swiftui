Loop through array elements
```swift
let platforms = ["iOS", "macOS", "tvOS", "watchOS"]

for os in platforms {
    print("Swift works great on \(os).")
}
```

Range loop
```swift
for i in 1...5 {
    print("Counting from 1 through 5: \(i)")
}

for i in 1..<5 {
    print("Counting 1 up to 5: \(i)")
}
```

Loop without using loop variable
```swift
var lyric = "Haters gonna"

for _ in 1...5 {
    lyric += " hate"
}
```
