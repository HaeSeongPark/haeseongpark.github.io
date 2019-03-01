---
title:  "The Big Nerd Ranch Swift - Ch.25 Gold Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

It is similar to ch24 Bronze Challenge. I went ahead...
Creat Person Class and have it conform Equatable Protocl. and implement == method.

```swift
class Person: Equatable {
    
    var name: String
    var age: Int
    
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
    
    static func == (lhs: Person, rhs: Person) -> Bool {
        return ( lhs.name == rhs.name ) && ( lhs.age == rhs.age )
    }
}

```
And test it
```swift
let p1 = Person(name: "p1", age: 1)
let p2 = Person(name: "p2", age: 2)
var people = [p1, p2]
let p1Index = people.firstIndex(of: p1)  // 0
````


  [code1](https://github.com/HaeSeongPark/BNRSwift/blob/master/25Comparison.playground/Pages/Chapter25.xcplaygroundpage/Contents.swift#L66) &nbsp; [code2](https://github.com/HaeSeongPark/BNRSwift/blob/master/25Comparison.playground/Pages/Chapter25.xcplaygroundpage/Contents.swift#L82)