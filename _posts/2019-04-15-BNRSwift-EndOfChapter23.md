---
title:  "The Big Nerd Ranch Swift - End of chapter 23"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift

---
## Summary
- Protocol Extension
 - In this chapter, You can learn how to extension protocol without or with where clauses and default implementation for the protocol's own requirements. Also you encounter tricky thing which is duplicated property when you use protocol extension. See the title propery in the code following.

```swift
// abbreviated version 

struct EllipticalWorkout:Exercise {
    let name = "Elliptical Workout"
    let title = "Workout using the Go Fast Elliptical Trainer 3000" // EllipticalWorkout's own property --- 1
    let caloriesBurned: Double
    let minutes: Double
}

extension Exercise {
    var title: String {  // added property using extension --- 2
        return "\(name) - \(minutes) muntures"
    }
}

for exercise in mondayWorkout {
    print(exercise.title)  // --- 2
}

print(ellipticalWorkOut.title) // --- 1
```

Unfortunately, It's valid syntax. No errors. So It's so confusing which string would be printed. May be not. Because of single duplicated property. 
And You will know which string would be printed if you read the description of the book easyliy. But if there are other things like that, source code  would be so difficult to read. So be careful add property using extension. Especially, when you add property or method in type made by apple.(Is it called standard library or frameowrk?)

[source code](https://github.com/HaeSeongPark/BNRSwift/commit/8078444636e2fdbc5858af2f4cd1e89d0b2cf27b)