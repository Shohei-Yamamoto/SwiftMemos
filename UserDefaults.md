# UserDefaults

# Encode

Struct should be codable to encode and store in UserDefaults.

```swift
struct Item: Codable {
  ...
}

let encoder = JSONEncoder()
if let encoded = try? encoder.encode(item) {
  UserDefaults.standard.set(encoded, forKey: "Item")
 }
 ```

# Decode

```swift
if let item = UserDefaults.standard.data(forKey: "Item) {
  let decoder = JSONDecoder()
  let decoded = try? decoder.decode([ExpenseItem].self, from: items)
}

```


# Codable
If you want to save pre-initialized UUID in UserDefault, use variable or the UUID is created every time. 

```swift
struct Item: Codable {
    let id = UUID() // warning: Immutable property will not be decoded because it is declared with an initial value which cannot be overwritten
    let name: String
}
```
