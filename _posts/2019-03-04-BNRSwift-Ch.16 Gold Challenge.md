---
title:  "The Big Nerd Ranch Swift - Ch.16 Gold Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'. And in changePopulation method of town, when amout is less than 0 notify mayor

Make anxietyLevel property in Mayor and related method to increase anxietyLevel. 

```swift
struct Mayor {
    private var anxietyLevel = 0
    ...
     mutating func listenZombieAttact() {
        anxietyLevel += 10
    }
}

// struct Town
    mutating func changePopulation(by amount: Int) {
        population += amount
        
        if ( amount < 0 ) {
            mayor.listenZombieAttact()
        }
    }
```

  [code1](https://github.com/HaeSeongPark/BNRSwift/blob/master/16MonsterTown/MonsterTown/Mayor.swift#L13) &nbsp; [code2](https://github.com/HaeSeongPark/BNRSwift/blob/master/16MonsterTown/MonsterTown/Mayor.swift#L31) &nbsp; [code3](https://github.com/HaeSeongPark/BNRSwift/blob/master/16MonsterTown/MonsterTown/Town.swift#L58)
