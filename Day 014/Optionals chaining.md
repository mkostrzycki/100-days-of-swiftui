```swift
let names = ["Arya", "Bran", "Robb", "Sansa"]

let chosen = names.randomElement()?.uppercased() ?? "No one"
print("Next in line: \(chosen)")
```

```swift
struct Book {
    let title: String
    let author: String?
}

var book: Book? = nil
let author = book?.author?.first?.uppercased() ?? "A"
print(author)
```

```swift
var catalogue : Dictionary? = ["Lotus" : (minPrice: 50, maxPrice: 200)]

var lotus = catalogue?["Lotus"]

if let price = catalogue?["Lotus"]?.minPrice {
    print("The minimum price is \(price)")
}
// prints "The minimum price is 40"
```

```swift
class DriversLicence {
    var pointsOnLicence = 0

    func isValidForVehicle(vehicle : Vehicle) -> Bool {
        // ...
        return true
    }
}

class Vehicle {
    var owner: Person?
}

class Person {
    var licence : DriversLicence?
}

let andy = Person()
andy.licence = DriversLicence()
let car = Vehicle()
car.owner = andy

if let canDriveVehicle = andy.licence?.isValidForVehicle(car) {
    if (canDriveVehicle) {
        print("Andy's licence allows him to drive the car.")
    } else {
        print("Andy's license doesn't allow him to drive the car.")
    }
} else {
    print("Andy doesn't have a licence.")
}
// Prints "Andy's licence allows him to drive the car."
```

We can also set values using optional chaining
```swift
struct Book {
    let title: String
    var author: String?
}

let author = "Andrzej Sapkowski"
var book: Book? = nil
book?.author = author
```

