Make a class hierarchy for animals, starting with `Animal` at the top, then `Dog` and `Cat` as subclasses, then `Corgi` and `Poodle` as subclasses of `Dog`, and `Persian` and `Lion` as subclasses of `Cat`. 

But there’s more:
1. The `Animal` class should have a `legs` integer property that tracks how many legs the animal has.
2. The `Dog` class should have a `speak()` method that prints a generic dog barking string, but each of the subclasses should print something slightly different.
3. The `Cat` class should have a matching `speak()` method, again with each subclass printing something different.
4. The `Cat` class should have an `isTame` Boolean property, provided using an initializer.

```swift
class Animal {
    let legs: Int

    init(legs: Int) {
        self.legs = legs
    }
}

class Dog: Animal {
    init() {
        super.init(legs: 4)
    }

    func speak() {
        print("Woof!")
    }
}

class Cat: Animal {
    var isTame: Bool

    init(isTame: Bool) {
        self.isTame = isTame
        super.init(legs: 4)
    }

    func speak() {
        print("Meow!")
    }
}

class Corgi: Dog {
    override func speak() {
        print("Corgi woof!")
    }
}

class Poodle: Dog {
    override func speak() {
        print("Poodle woof!")
    }
}

class Persian: Cat {
    init() {
        super.init(isTame: true)
    }

    override func speak() {
        print("Mrrrraauuu!")
    }
}

class Lion: Cat {
    init() {
        super.init(isTame: false)
    }

    override func speak() {
        print("Rooaaarrr!")
    }
}
```