---
title:  "The Big Nerd Ranch Swift - Ch.16 Bronze Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

Simple, if newPopulation is less than Population, print noticeable message. To do this, there are two cases. You can use willSet, and didSet.

```swift
// class Town...
        willSet(newPopulation) {
            if ( newPopulation < population ) {
                print("warning! population has lowered")
                ......
            }
        }
/// If you use didSet, code would be following...
        willSet(oldPopulation) {
            if ( population < oldPopulation ) {
                print("warning! population has lowered")
                ......
            }
        }
```

  [code](https://github.com/HaeSeongPark/BNRSwift/blob/master/16MonsterTown/MonsterTown/Town.swift#L15)
