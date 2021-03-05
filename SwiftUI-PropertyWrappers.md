# State
@State is only used in View and attached to struct.
It can be attached to class, but SwiftUI can't notice the change of the state.
When struct variable is changed and the copy is stored, SwiftUI notice that and reload the whole view.
Class is reference type which isn't copied on change. 

```swift 
@State private var flag = false
```


# ObservableObject
@ObservableObject, @Published, @ObservedObject are used for classes.
@Published is attached to the @ObservableObject classes' property which you want to let SwiftUI know the value change.


```swift
class Test: ObservableObject {
  @Published var items = [String]()
}

struct ContentView: View {
  @ObservableOnject var test = Test()
}

```
