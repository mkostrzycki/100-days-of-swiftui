Make a protocol that describes a building, adding various properties and methods, then create two structs, `House` and `Office`, that conform to it. Your protocol should require the following:

1. A property storing how many rooms it has.
2. A property storing the cost as an integer (e.g. 500,000 for a building costing $500,000.)
3. A property storing the name of the estate agent responsible for selling the building.
4. A method for printing the sales summary of the building, describing what it is along with its other properties.

```swift
protocol Building {
    var roomsCount: Int { get }
    var cost: Int { get }
    var estateAgentName: String { get }
    
    func saleSummary() -> String
}

extension Building {
    func saleSummary() -> String {
        "This building with \(roomsCount) rooms was sell by \(estateAgentName) for $\(cost)."
    }
}

struct House: Building {
    let roomsCount: Int
    let cost: Int
    let estateAgentName: String
}

struct Office: Building {
    let roomsCount: Int
    let cost: Int
    let estateAgentName: String
}

var myHouse = House(roomsCount: 3, cost: 600_000, estateAgentName: "Dexter Morgan")
var myOffice = Office(roomsCount: 2, cost: 450_000, estateAgentName: "Luke Skywalker")

print(myHouse.saleSummary()) // This building with 3 rooms was sell by Dexter Morgan for $600000.
print(myOffice.saleSummary()) // This building with 2 rooms was sell by Luke Skywalker for $450000.
```

