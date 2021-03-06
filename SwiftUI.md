# Identifiable

You can attach this protocol to structs that has `id` property.
This protocol avoid us to write id in ForEach.

```swift
struct Item: Identifiable {
    let id = UUID()
    let name: String
}

var items = [Item]()

ForEach(items) { item in
    Text(item.name)
}
```
