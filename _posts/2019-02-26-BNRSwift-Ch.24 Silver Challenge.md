---
title:  "The Big Nerd Ranch Swift - Ch.24 Silver Challenge"
categories: 
  - Swift
tags:
  - BigNerdRanchSwift
---

> There is no description of challenge. Becaouse of license.

When person take ownership of asset, check if asset is already owned by others. if it is print notable messages

> When I use a header "class someName..." in code block for some code, that means the following code is within the scope of the class named 'someName'.

```swift
// class Person...
    func takeOwnershipOfAsset(asset:Asset){
        if asset.owner == nil {
            accountant.gainedNewAsset(asset: asset) {
                asset.owner = self
                assets.append(asset)
            }
        } else {
            print("asset is already owend by \(asset.owner!.name.debugDescription)")
        }
        
    }
```

[source code](https://github.com/HaeSeongPark/BNRSwift/blob/master/24CyclicalAssets/CyclicalAssets/Person.swift#L33)

> This Challenge is not related in this chapter like memory management, cycle etc. It would be good challenge would related this chapter directly.