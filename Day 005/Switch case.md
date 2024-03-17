```swift
enum Weather {
    case sun, rain, wind, snow, unknown
}

let forecast = Weather.sun

switch forecast {
case .sun:
    print("It should be a nice day.")
case .rain:
    print("Pack an umbrella.")
case .wind:
    print("Wear something warm")
case .snow:
    print("School is cancelled.")
case .unknown:
    print("Our forecast generator is broken!")
default:
	print("Default message!")
}
```

If you’ve ever used other programming languages, you might have noticed that Swift’s `switch`statement is different in two places:

1. All `switch` statements _must_ be exhaustive, meaning that all possible values must be handled in there so you can’t leave one off by accident.
2. Swift will execute the first case that matches the condition you’re checking, but no more. Other languages often carry on executing other code from all subsequent cases, which is usually entirely the wrong default thing to do.

If you explicitly _want_ Swift to carry on executing subsequent cases, use `fallthrough`. This is _not_ commonly used, but sometimes – just sometimes – it can help you avoid repeating work.
```swift
let day = 5
print("My true love gave to me…")

switch day {
case 5:
    print("5 golden rings")
    fallthrough
case 4:
    print("4 calling birds")
    fallthrough
case 3:
    print("3 French hens")
    fallthrough
case 2:
    print("2 turtle doves")
    fallthrough
default:
    print("A partridge in a pear tree")
}
```

`fallthrough` does not check other conditions but just run case code.