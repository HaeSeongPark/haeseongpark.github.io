---
title:  "The Big Nerd Ranch Swift - Ch.20 Gold Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

First, Add a multiplication and division Token

```swift
enum Token {
    case number(value : Int, position : Int)
    case minus(position : Int)
    case plus(position: Int)
    case multiply(postion : Int)
    case divide(position : Int)
}
```
Add some code related it 
```swift
class lexer ...
func lex() {
    ...
    case "*":
        tokens.append(.multiply(postion: distanceToPosition))
        advance()
    case "/":
        tokens.append(.divide(position: distanceToPosition))
        advance()
    ...
}
```                
Add some code related it. This is important point.
In math, multiplication and division have higher precendence than addition and subtraction.
So, We have to deal with multiplication and division first then addition and subtraction.
This idea is "recursive descent parser". Google it.

```swift
class Parser...


func parse() {
        func parse() throws -> Int {
        // Require a number first
        var value = try getNumber()
        
        while let token = getNextToken() {
            switch token {
            // Getting a Plus after a Number is legal
            case .plus:
                // After a plus, we must get another number
                let nextNumber = try parse()
                value += nextNumber
            case .minus:
                let nextNumber = try parse()
                value -= nextNumber
            case .multiply:
                let nextNumber = try getNumber()
                value *= nextNumber
            case .divide:
                let nextNumber = try getNumber()
                value /= nextNumber
            case .number(let value, let position):
                throw Error.InvalidToken(position: position, invalidToken: String(value))
            }
        }
        return value
    }
}

[code](https://github.com/HaeSeongPark/BNRSwift/commit/54f1fea9861272d899a6e001ca3d3b8a5d4a21eb)
