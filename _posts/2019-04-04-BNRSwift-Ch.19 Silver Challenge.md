---
title:  "The Big Nerd Ranch Swift - Ch.19 Silver Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

I added maxLengthOfLabelForColumn func in TabularDataSource protocol to calcutlate max lenght of label of each column and use it when calculate padding

```swift
protocol TabularDataSource {
    ...
    func maxLengthOfLabelForColumn(column:Int) -> Int
    ... 
}

 let paddingAmount = dataSource.maxLengthOfLabelForColumn(column: j) - itemString.count

 /// implementing code in department struc
    func maxLengthOfLabelForColumn(column:Int) -> Int {
      let extraPadding = 3
      var result = columnLabels[column].count

      for person in people {
          if person[column].count > result {
              result = person[column].count
          }
      }
      
      return result + extraPadding
  }
```



  [code](https://github.com/HaeSeongPark/BNRSwift/blob/master/19Protocols.playground/Contents.swift)
