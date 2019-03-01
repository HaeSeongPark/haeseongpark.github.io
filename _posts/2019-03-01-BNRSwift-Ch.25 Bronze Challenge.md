---
title:  "The Big Nerd Ranch Swift - Ch.25 Bronze Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

1. overload the + operator

```swift
// class Point...
    static func + (lhs:Point, rhs: Point) -> Point {
        return Point(x: lhs.x + rhs.x,
                     y: lhs.y + rhs.y)
    }
```

  [code1](https://github.com/HaeSeongPark/BNRSwift/blob/master/25Comparison.playground/Pages/Chapter25.xcplaygroundpage/Contents.swift#L39)  &nbsp;  [code2](https://github.com/HaeSeongPark/BNRSwift/blob/master/25Comparison.playground/Pages/Chapter25.xcplaygroundpage/Contents.swift#L63)
