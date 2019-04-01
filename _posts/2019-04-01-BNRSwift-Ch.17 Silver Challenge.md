---
title:  "The Big Nerd Ranch Swift - Ch.17 Silver Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

I added covenience keyword at required init of zombie class and call designated initializer.

```swift
class Zombie...
    convenience required init?(town: Town?, monsterName: String) {
        self.init(limp:false, fallingApart:false, town:town, monsterName:monsterName)
    }
```

  [code](https://github.com/HaeSeongPark/BNRSwift/blob/master/17MonsterTown/MonsterTown/Zombie.swift#L31)
