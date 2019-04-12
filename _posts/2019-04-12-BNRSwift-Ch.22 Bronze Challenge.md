---
title:  "The Big Nerd Ranch Swift - Ch.22 Bronze Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

I made the filter function that take a clousure as argument and return Element's array.
And then I go though all items in stack whether item is valid in closure.

```Swift
struct stack...
    func filter(_ isIncluded: (Element) -> Bool) -> [Element] {
        var result = [Element]()
        for item in items {
            if isIncluded(item) {
                result.append(item)
            }
        }
        return result
    }
```
And use it. You can say any other form of clousre
```Swift 
let evenNumbers = myStack.filter { $0 % 2 == 0}
```

  [code](https://github.com/HaeSeongPark/BNRSwift/commit/a4306bae83db9e2341dab72db0cd665d966a5a02)
