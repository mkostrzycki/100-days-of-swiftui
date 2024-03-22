```swift
func getRandomNumber() -> some Equatable {
    Int.random(in: 1...6)
}

func getRandomBool() -> some Equatable {
    Bool.random()
}
```

The advantage here is that Swift always knows the real underlying data type. It’s a subtle distinction, but returning `Vehicle` means "any sort of Vehicle type but we don't know what", whereas returning `some Vehicle` means "a specific sort of `Vehicle` type but we don't want to say which one.”