```swift
let people = Set(["Denzel Washington", "Tom Cruise", "Nicolas Cage", "Samuel L Jackson"])
```

Create empty set and insert data
```swift
var people = Set<String>()
people.insert("Denzel Washington")
people.insert("Tom Cruise")
people.insert("Nicolas Cage")
people.insert("Samuel L Jackson")
```

Set doesn't have order so we use `insert` and not `append` like in array.

Sets are unordered and cannot contain duplicates, whereas arrays retain their order and _can_ contain duplicates.
Sets are way more efficient when we need to check if set contains specific element. For example, if you want to check whether a word appears in a dictionary, you should use a set: you don’t have duplicates, and you want to do a fast look up.