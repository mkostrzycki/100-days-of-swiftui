1. Add the launch date to `MissionView`, below the mission badge. You might choose to format this differently given that more space is available, but it’s down to you.
2. Extract one or two pieces of view code into their own new SwiftUI views – the horizontal scroll view in `MissionView` is a great candidate, but if you followed my styling then you could also move the `Rectangle` dividers out too.
3. For a tough challenge, add a toolbar item to `ContentView` that toggles between showing missions as a grid and as a list.

**Tip:** For that last one, your best bet is to make all your grid code and all your list code two separate views, and switch between them using an `if` condition in `ContentView`. You can’t attach SwiftUI modifiers to an `if` condition, but you can wrap that condition in a `Group` then attach modifiers to there, like this:

```swift
Group {
    if showingGrid {
        GridLayout(astronauts: astronauts, missions: missions)
    } else {
        ListLayout(astronauts: astronauts, missions: missions)
    }
}
.navigationTitle("My Group")
```

You might hit some speed bumps trying to style your list, because they have a particular look and feel on iOS by default. Try attaching `.listStyle(.plain)` to your list, then something like `.listRowBackground(Color.darkBackground)` to the contents of your list row – that should get you a long way towards your goal.

Challenge solved in repository -> https://github.com/mkostrzycki/100dos-Project08-Moonshot