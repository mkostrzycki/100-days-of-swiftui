Write a function that accepts an integer from 1 through 10,000, and returns the integer square root of that number. That sounds easy, but there are some catches: 

1. You can’t use Swift’s built-in `sqrt()` function or similar – you need to find the square root yourself.
2. If the number is less than 1 or greater than 10,000 you should throw an “out of bounds” error.
3. You should only consider integer square roots – don’t worry about the square root of 3 being 1.732, for example.
4. If you can’t find the square root, throw a “no root” error.

```swift
enum IntSqrtErrors: Error {
    case OutOfBounds, NoIntRoot
}

func intSqrt(from: Int) throws -> Int {
    if (from < 1) || (from > 10_000) {
        throw IntSqrtErrors.OutOfBounds
    }
    
    var root = 0
    // brute force method :)
    for i in 1...100 {
        if i*i == from {
            root = i
            break
        }
    }
    
    if root == 0 {
        throw IntSqrtErrors.NoIntRoot
    } else {
        return root
    }
}

do {
    let number = 64
    let root = try intSqrt(from: number)
    print(root)
} catch IntSqrtErrors.OutOfBounds {
    print("Use integer between 1 and 10 000")
} catch IntSqrtErrors.NoIntRoot {
    print("There is no integer root for given number")
} catch {
    print(error.localizedDescription)
}
```