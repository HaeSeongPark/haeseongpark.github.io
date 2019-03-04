---
title:  "The Big Nerd Ranch Swift - Ch.16 Silver Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

First, make new type called mayor as struct. And make new instance method and print the message in case of polulation has lowed. Finllay, In town, if population has lowed, notify mayor.

```swift
struct Mayor {

    ... 
        
    enum PopulationChanged {
        case decrease
        case increase
    }
    
    func listen(to populationChagnd: PopulationChanged) {
        switch populationChagnd {
        case .decrease:
            print("I'm deeply saddened to hear about this lastes tragedy. I promise that my office is looking into the nature of this rash of violence.")
        case .increase:
            break // noting to do
        }
    }
}

// population willset of struct town...

 mayor.listen(to: .decrease)
```

  [code](https://github.com/HaeSeongPark/BNRSwift/blob/master/16MonsterTown/MonsterTown/Mayor.swift) &nbsp; [code1](https://github.com/HaeSeongPark/BNRSwift/blob/master/16MonsterTown/MonsterTown/Town.swift#L21)
