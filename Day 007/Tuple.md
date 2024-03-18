```swift
func getUser() -> (firstName: String, lastName: String) {
    (firstName: "Taylor", lastName: "Swift")
}

let user = getUser()
print("Name: \(user.firstName) \(user.lastName)")
```

Tuples seem awfully similar to dictionaries, but they are different:

1. When you access values in a dictionary, Swift can’t know ahead of time whether they are present or not. Yes, we knew that `user["firstName"]` was going to be there, but Swift can’t be sure and so we need to provide a default value.
2. When you access values in a tuple, Swift _does_ know ahead of time that it is available because the tuple _says_ it will be available.
3. We access values using `user.firstName`: it’s not a string, so there’s also no chance of typos.
4. Our dictionary might contain hundreds of other values alongside `"firstName"`, but our tuple can’t – we must list all the values it will contain, and as a result it’s guaranteed to contain them all and nothing else.

So, tuples have a key advantage over dictionaries: we specify exactly which values will exist and what types they have, whereas dictionaries may or may not contain the values we’re asking for.

### When should you use an array, a set, or a tuple in Swift?
Arrays keep the order and can have duplicates, sets are unordered and _can’t_ have duplicates, and tuples have a fixed number of values of fixed types inside them. 

So:

- If you want to store a list of all words in a dictionary for a game, that has no duplicates and the order doesn’t matter so you would go for a set.
- If you want to store all the articles read by a user, you would use a set if the order didn’t matter (if all you cared about was whether they had read it or not), or use an array if the order _did_ matter.
- If you want to store a list of high scores for a video game, that has an order that matters and might contain duplicates (if two players get the same score), so you’d use an array.
- If you want to store items for a todo list, that works best when the order is predictable so you should use an array.
- If you want to hold precisely two strings, or precisely two strings and an integer, or precisely three Booleans, or similar, you should use a tuple.