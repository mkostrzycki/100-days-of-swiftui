```swift
let employee = [
    "name": "Taylor Swift",
    "job": "Singer", 
    "location": "Nashville"
]
```
It's like array with `key: value`

Read data using keys
```swift
print(employee2["name"]) // Taylor Swift
print(employee2["job"]) // Singer
print(employee2["location"]) // Nashville
```

Key may not exist so it's good to provide default value
```swift
print(employee2["name", default: "Unknown"])
print(employee2["job", default: "Unknown"])
print(employee2["location", default: "Unknown"])
```

Other data types for keys and values
```swift
let olympics = [
    2012: "London",
    2016: "Rio de Janeiro",
    2021: "Tokyo"
]

print(olympics[2012, default: "Unknown"]) // London
```

Create empty dictionary
```swift
var heights = [String: Int]()
heights["Yao Ming"] = 229
heights["Shaquille O'Neal"] = 216
heights["LeBron James"] = 206
```
