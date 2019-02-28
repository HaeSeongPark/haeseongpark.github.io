---
title:  "The Big Nerd Ranch Swift - Ch.24 Bronze Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

Add remove method to Person (removeOwnershipOfAsset(asset:) in my case) . And make sure person have right asset which is about to remvoe.  if the asset is found, invoke remoteNesAsset method of Account class which is not yet implemtented. and add the following two line to completion closure. In this situation, there are two case, one is to use firstIndex(where:) second is to use firstIndex(of:).

```swift
// class Person...
  func removeOwnershipOfAsset(asset:Asset) {
//        if assets.firstIndex(where: {($0.name == asset.name && $0.value == asset.value)}) {
//            
//        }
        
      if let i = assets.firstIndex(of: asset) {
          accountant.removeNewAsset(asset: asset) {
            asset.owner = nil
            assets.remove(at: i)
         }
      }
    }
```

For the second, we have to make Asset class conform to Equatable protocol. 

```swift
// class Asset...
  class Asset: CustomStringConvertible, Equatable {
    ...
    static func == (lhs: Asset, rhs: Asset) -> Bool {
    return (lhs.name == rhs.name ) && (lhs.value == rhs.value)
    }
  }
```

Finally make remove method to Account class. 

```swift
// class Account...
func removeNewAsset(asset: Asset, completion: () -> Void ) {
    netWorth -= asset.value
    completion()
}

```

[source code](https://github.com/HaeSeongPark/BNRSwift/tree/master/24CyclicalAssets/CyclicalAssets)

> This Challenge is not related in this chapter like memory management, cycle etc. It would be good challenge would related this chapter directly.