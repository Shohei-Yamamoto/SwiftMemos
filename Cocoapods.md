
# m1 mac cocoapods
I couldn't execute `pod install`

How to solve the problem.
1. rosettaでterminalを起動(FinderでTerminalの情報を見る > Rosettaで起動)
2. `sudo gem install ffi`
3. `pod install`


* [M1 Macでpod installを実行する](https://zenn.dev/akeome/articles/2433d792db022835c7e7)


# error on building
`building for iOS Simulator, but linking in object file built for iOS, for architecture arm64
clang: error: linker command failed with exit code 1 (use -v to see invocation)`

[[iOS] Xcode12.0で「building for iOS Simulator, but linking in object file ... for architecture arm64」エラーの対処法: ものづくりログ](http://blog.be-style.jpn.com/article/187942746.html)

```
Could not find module 'RealmSwift' for target 'arm64-apple-ios-simulator'; found: x86_64-apple-ios-simulator, x86_64
```

1. I set `Build Active Architecture Only: Debug` to `No`
2. I set `Excluded Architectures: Debug` to `x86_64`


# migration to swift package manager

1. move to directory and `pod deintegrate`
2. remove unneccesary files such as `.xcworkspace`, `Podfile`
3. Add package with swift package manager.

[CocoaPodsからSwift Package Managerへ移行するには | 株式会社ブリッツゲート](https://blitzgate.co.jp/blog/2234/)
