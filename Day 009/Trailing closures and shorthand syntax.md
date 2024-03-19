```swift
// we can shorten this closure
let captainFirstTeam = team.sorted(by: { (name1: String, name2: String) -> Bool in
    if name1 == "Suzanne" {
        return true
    } else if name2 == "Suzanne" {
        return false
    }

    return name1 < name2
})

// like that - we do not need to provide types in this case and we can skip parameter name "by" with parenthesis (trailing closure)
let captainFirstTeam = team.sorted { name1, name2 in
    if name1 == "Suzanne" {
        return true
    } else if name2 == "Suzanne" {
        return false
    }

    return name1 < name2
}

// Swift can provide also parameters names so we can skip them (shorthand syntax)
let captainFirstTeam = team.sorted {
    if $0 == "Suzanne" {
        return true
    } else if $1 == "Suzanne" {
        return false
    }

    return $0 < $1
}
```

Skipping parameters names is useful with one-line closures
```swift
let reverseTeam = team.sorted {
    return $0 > $1
}

// we can skip "return" in one-line function
let reverseTeam = team.sorted { $0 > $1 }

// other examples
let tOnly = team.filter { $0.hasPrefix("T") }

let uppercaseTeam = team.map { $0.uppercased() }
```
