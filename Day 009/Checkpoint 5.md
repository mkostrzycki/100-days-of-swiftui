You’ve already met `sorted()`, `filter()`, `map()`, so I’d like you to put them together in a chain – call one, then the other, then the other back to back without using temporary variables.

Your input is this: 

```swift
let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]
```

Your job is to:

1. Filter out any numbers that are even
2. Sort the array in ascending order
3. Map them to strings in the format “7 is a lucky number”
4. Print the resulting array, one item per line

So, your output should be as follows:

```swift
7 is a lucky number
15 is a lucky number
21 is a lucky number
31 is a lucky number
33 is a lucky number
49 is a lucky number
```

### Version 1
```swift
let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]

let filterEven: (Int) -> Bool = { $0 % 2 != 0 }
let mapToString: (Int) -> String = { "\($0) is a lucky number" }

for element in luckyNumbers.filter(filterEven).sorted().map(mapToString) {
    print(element)
}
```

Here are some hints:

1. You need to use the `filter()`, `sorted()`, and `map()` functions.
2. The order you run the functions matters – if you convert the array to a string first, `sorted()` will do a string sort rather than an integer sort. That means 15 will come before 7, because Swift will compare the “1” in “15” against “7”.
3. To chain these functions, use `luckyNumbers.first { }.second { }`, obviously putting the real function calls in there.
4. You should use `isMultiple(of:)` to remove even numbers.
### Version 2 (following hints)
```swift
let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]

for element in luckyNumbers.filter({ !$0.isMultiple(of: 2) }).sorted().map({ "\($0) is a lucky number" }) {
    print(element)
}
```

