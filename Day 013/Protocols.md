Protocols let us define how structs, classes, and enums ought to work: what methods they should have, and what properties they should have.

```swift
protocol Vehicle {
    var name: String { get }
    var currentPassengers: Int { get set }
    func estimateTime(for distance: Int) -> Int
    func travel(distance: Int)
}
```

`Car` conform to `Vehicle` protocol
```swift
struct Car: Vehicle {
	let name = "Car"
	var currentPassengers = 1

    func estimateTime(for distance: Int) -> Int {
        distance / 50
    }

    func travel(distance: Int) {
        print("I'm driving \(distance)km.")
    }

    func openSunroof() {
        print("It's a nice day!")
    }
}
```

Then we can use protocol as a type
```swift
func getTravelEstimates(using vehicles: [Vehicle], distance: Int) {
    for vehicle in vehicles {
        let estimate = vehicle.estimateTime(for: distance)
        print("\(vehicle.name): \(estimate) hours to travel \(distance)km")
    }
}
```
