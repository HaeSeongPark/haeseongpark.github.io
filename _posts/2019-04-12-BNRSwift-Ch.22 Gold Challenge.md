---
title:  "The Big Nerd Ranch Swift - Ch.22 Gold Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'. And in changePopulation method of town, when amout is less than 0 notify mayor

I made function findAllUsingCollection. Its syntax is similar to pushItemsOntoStack funcion. It add constraints. T must conform Collection, U must conforom Equatable, element of T must be the same as the U. And Its logic is same. But return type and syntax is slightly changed.

```swift
struct stack...
func findAllUsingCollection<T:Collection, U:Equatable>(_ colleecion:T, _ elementToFind:U) -> [T.Index] where T.Iterator.Element == U {
    var result = [T.Index]()
    var index = colleecion.startIndex

    for item in colleecion {
        if item == elementToFind {
            result.append(index)
        }
        index = colleecion.index(after: index)
    }
    return result
}
```
And I found a elegant solution. not answer but read it worth.

```swift
// https://forums.bignerdranch.com/t/bronze-silver-gold-challenges-ch-22/10752/3
extension Collection where Iterator.Element: Equatable {
    func findAll(_ element: Iterator.Element) -> [Index] {
        return indices.reduce([]) {
            element == self[$1] ? $0 + [$1] : $0
        }
    }
}
$0 is array which is result, [Index]
$1 index (first...last)
```

  [code](https://github.com/HaeSeongPark/BNRSwift/commit/b8d9d51ef8773841972bc49e199e516780a0b31b)