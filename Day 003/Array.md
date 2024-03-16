```swift
var beatles = ["John", "Paul", "George", "Ringo"]
let numbers = [4, 8, 15, 16, 23, 42]
var temperatures = [25.3, 28.2, 26.4]
```

Swift counts an item's index from `0`.
```swift
print(beatles[0]) // John
print(numbers[1]) // 8
print(temperatures[2]) // 26.4
```

Append items
```swift
beatles.append("Allen")
beatles.append("Adrian")
beatles.append("Novall")
beatles.append("Vivian")
```

Swift does watch the _kind_ of data you’re trying to add, and will make sure your array only ever contains one type of data at a time.

Create an empty array
```swift
var scores = Array<Int>()
var albums = Array<String>()
var albums = [String]()
```

Count items in array
```swift
var characters = ["Lana", "Pam", "Ray", "Sterling"]
print(characters.count) // 4
```

Remove item on a specific index
```swift
characters.remove(at: 2)
print(characters.count) // 3
```

Remove all items
```swift
characters.removeAll()
print(characters.count) // 0
```

Check if array contains item
```swift
let bondMovies = ["Casino Royale", "Spectre", "No Time To Die"]
print(bondMovies.contains("Frozen")) // false
```

Sort array
```swift
let cities = ["London", "Tokyo", "Rome", "Budapest"]
print(cities.sorted()) // ["Budapest", "London", "Rome", "Tokyo"]
```

Reverse array
```swift
let presidents = ["Bush", "Obama", "Trump", "Biden"]
let reversedPresidents = presidents.reversed()
print(reversedPresidents) // ReversedCollection<Array<String>>(_base: ["Bush", "Obama", "Trump", "Biden"])
```

Swift doesn’t actually do the work of rearranging all the items, but instead just remembers to itself that you want the items to be reversed. So, when you print out `reversedPresidents`, don’t be surprised to see it’s not just a simple array any more - its reversed collection.