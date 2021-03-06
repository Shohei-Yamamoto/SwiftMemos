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
