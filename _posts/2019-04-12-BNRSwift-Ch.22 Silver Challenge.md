---
title:  "The Big Nerd Ranch Swift - Ch.22 Silver Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

I made the findAll function that takes two arguments. First One is elements in which we find Second one. I go though all elements and compare that element is equal Second one. And if it is, push it in findedIndexs. (foundedIndexes)

And then I go though all items in stack whether item is valid in closure.

```swift
func findAll<T:Equatable>(_ elements:[T],_ elementToFind:T) -> [Int] {
    var findedIndexs = [Int]()
    for (index, element) in elements.enumerated() {
        if element == elementToFind {
            findedIndexs.append(index)
        }
    }
    return findedIndexs
}

print(findAll([5,3,7,3,9], 3))

```



  [code](https://github.com/HaeSeongPark/BNRSwift/commit/0fcf931b3bdb08f32e3ac728eafed29af5f74e36)
