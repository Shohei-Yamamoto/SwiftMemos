# Count of days in the year

```swift
let range = Calendar.current.range(of: .day, in: .year, for: Date()) // 1..<366
range?.count // 365
```

# Count of weeks in the year

```swift
let range = Calendar.current.range(of: .weekOfYear, in: .year, for: Date()) // 1..<54
range?.count // 53
```

# weekDaySymbols
```swift
var calendar = Calendar.current
calendar.locale = Locale(identifier:  Locale.preferredLanguages.first!)
calendar.shortWeekdaySymbols // Sun, Mon, ...
```

# Previous Sunday

```swift
let components = Calendar.current.dateComponents([.year, .weekOfYear, .weekday], from: Date()) // year: 2021 weekday: 4 weekOfYear: 10 (2021/3/3 wed)
DateComponents(calendar: Calendar.current, year: components.year, weekday: 1, weekOfYear: components.weekOfYear).date // "Feb 28, 2021 at 12:00 AM"
```

> in the Gregorian calendar, n is 7 and Sunday is represented by 1.
[weekday | Apple Developer Documentation](https://developer.apple.com/documentation/foundation/nsdatecomponents/1410442-weekday)

# Locale

## get PreferedLocale
```swift
Locale(identifier:  Locale.preferredLanguages.first!)
```
