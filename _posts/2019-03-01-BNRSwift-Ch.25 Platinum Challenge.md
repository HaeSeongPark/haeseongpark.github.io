---
title:  "The Big Nerd Ranch Swift - Ch.25 Platinum Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

Make euclideanDistanceFromOrigin mothod in Point. and use it in `==` and `<` methods

```swift
// class Point...
    func euclideanDistanceFromOrigin() -> Double {
        return sqrt( Double(x * x) + Double(y * y) )
    }
    
    static func ==(lhs:Point, rhs:Point) -> Bool {
        return lhs.euclideanDistanceFromOrigin() == rhs.euclideanDistanceFromOrigin()
    }
    
    static func < (lhs: Point, rhs: Point) -> Bool {
        return lhs.euclideanDistanceFromOrigin() < rhs.euclideanDistanceFromOrigin()
    }
```
And test it
```swift 
let point1 = Point(x: 3, y: 4)
let point2 = Point(x: 2, y: 5)

let point1GreaterThanPoint2 = ( point1 > point2 ) // false
let point1LessThanPoint2 = ( point1 < point2 ) // true
let point1EqualToPoint2 = ( point1 == point2 ) // false
```


  [code1](https://github.com/HaeSeongPark/BNRSwift/blob/master/25Comparison.playground/Pages/Chapter25.xcplaygroundpage/Contents.swift#L25) &nbsp; [code2](https://github.com/HaeSeongPark/BNRSwift/blob/master/25Comparison.playground/Pages/Chapter25.xcplaygroundpage/Contents.swift#L88)