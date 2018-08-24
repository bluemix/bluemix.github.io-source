---
title: Synchronous Network Calls in Swift CLI
lang: en
direction: ltr
dir: ltr
date: 2018-05-08 19:11:17
tags:
	- Swift
	- Sync
	- Network
	- HTTP
	- JSON
	- Async Await
	- XCode
	- Swift Package Manager
---


[⚠️ Incomplete Article ]
### Swift Package Manager
swift package init --type executable
swift package generate-xcodeproj
swift build
.build/debug/CommandLineTool

```swift
// swift-tools-version:4.1
// The swift-tools-version declares the minimum version of Swift required to build this package.

import PackageDescription

let package = Package(
    name: "CommandLineTool",
    dependencies: [
        .package(
            url: "https://github.com/mxcl/PromiseKit",
            from: Version("6.0.0")
        ),
        .package(
            url: "https://github.com/yannickl/AwaitKit.git",
            from: Version("5.0.0")
        ),
        .package(
            url: "https://github.com/SwiftyJSON/SwiftyJSON.git",
            from: Version("4.0.0")
        )
    ],
    targets: [
        .target(
            name: "CommandLineTool",
            dependencies: ["CommandLineToolCore"]
        ),
        .target(
            name: "CommandLineToolCore",
            dependencies: ["PromiseKit", "AwaitKit", "SwiftyJSON"]
        )
    ]
)
```
### XCode

### PromiseKit

### AwaitKit

### SwiftyJSON

```swift
import Foundation
import PromiseKit
import AwaitKit
import SwiftyJSON

public final class CommandLineTool {
  private let arguments: [String]
  
  public init(arguments: [String] = CommandLine.arguments) {
    self.arguments = arguments
  }
  
  func fetch(url: URL) -> Promise<Data> {
    return Promise { seal in
      URLSession.shared.dataTask(with: url) { data, _, error in
        seal.resolve(data, error)
        }.resume()
    }
  }
  
  
  public func run() throws {
    
    print("fetching...")
    do {
      let data = try await(fetch(url: URL(string: "https://api.github.com/users/bluemix")!))
      print("JSON(data)[\"name\"]: \(JSON(data)["name"])")
      
    } catch {
      print("error: \(error)")
    }
  }
}

```