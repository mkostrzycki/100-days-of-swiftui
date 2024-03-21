Create a struct to store information about a car, including its model, number of seats, and current gear, then add a method to change gears up or down. Have a think about variables and access control: what data should be a variable rather than a constant, and what data should be exposed publicly? Should the gear-changing method validate its input somehow (valid gears 1...10)?

```swift
struct Car {
    let model: String
    let seatsNumber: Int
    private(set) var currentGear: Int
    
    private let minGear = 1
    private let maxGear = 10
    
    init(model: String, seats: Int) {
        self.model = model
        self.seatsNumber = seats
        self.currentGear = minGear
        print("Hi, i'm your new car \(model) and I can take \(seatsNumber) people with me.")
    }
    
    mutating func gearUp() -> Bool {
        if currentGear < maxGear {
            currentGear += 1
            print("We are on gear \(currentGear) now")
            return true
        } else {
            print("We are on highest gear already!")
            return false
        }
    }
    
    mutating func gearDown() -> Bool {
        if currentGear > minGear {
            currentGear -= 1
            print("We are on gear \(currentGear) now")
            return true
        } else {
            print("We are on lowest gear already!")
            return false
        }
    }
}

var myNewShinnyCar = Car(model: "Toyota Mirai", seats: 5) // Hi, i'm your new car Toyota Mirai and I can take 5 people with me.
print("Let's ride baby!")
myNewShinnyCar.gearUp() // We are on gear 2 now
myNewShinnyCar.gearUp() // We are on gear 3 now
myNewShinnyCar.gearUp() // We are on gear 4 now
print("Slow down boy!")
myNewShinnyCar.gearDown() // We are on gear 3 now
myNewShinnyCar.gearDown() // We are on gear 2 now
myNewShinnyCar.gearDown() // We are on gear 1 now
myNewShinnyCar.gearDown() // We are on lowest gear already!
```

