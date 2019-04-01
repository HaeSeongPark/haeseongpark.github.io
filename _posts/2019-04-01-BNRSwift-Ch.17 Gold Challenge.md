---
title:  "The Big Nerd Ranch Swift - Ch.17 Gold Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'. And in changePopulation method of town, when amout is less than 0 notify mayor

Change the init with failable init in Mosnter and Zombie which is subclass of Monster. If you change the init withh failable init, you have to change the related init too. Otherwise, You will see a number of errors that you have to fix

```swift
class Monster...
    required init?(town: Town?, monsterName:String) {
        ...
    }
class Zombie...
    init?(limp: Bool, fallingApart:Bool, town:Town?, monsterName:String) {
        ...
        super.init(town: town, monsterName: monsterName)

    }

    convenience init?(limp:Bool, fallingApart:Bool) {
        self.init(limp:limp, fallingApart: fallingApart, town:nil, monsterName:"Fred")
        ...
    }
    
    convenience required init?(town: Town?, monsterName: String){
        self.init(limp:false, fallingApart:false, town:town, monsterName:monsterName)
    }

```

  [code](https://github.com/HaeSeongPark/BNRSwift/tree/master/17MonsterTown/MonsterTown)