# AlamofireSafariLogger - a lightweight Alamofire call debugger

[![CI Status](http://img.shields.io/travis/rudolphwong2002@gmail.com/AlamofireSafariLogger.svg?style=flat)](https://travis-ci.org/rudolphwong2002@gmail.com/AlamofireSafariLogger)
[![Version](https://img.shields.io/cocoapods/v/AlamofireSafariLogger.svg?style=flat)](http://cocoapods.org/pods/AlamofireSafariLogger)
[![License](https://img.shields.io/cocoapods/l/AlamofireSafariLogger.svg?style=flat)](http://cocoapods.org/pods/AlamofireSafariLogger)
[![Platform](https://img.shields.io/cocoapods/p/AlamofireSafariLogger.svg?style=flat)](http://cocoapods.org/pods/AlamofireSafariLogger)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

- iOS 8.0+
- Xcode 8.0+
- Swift 3.2+

## Usage
This project is inspired by AlamofireNetworkActivityLogger and facebook Stetho library.
Reference:
https://github.com/konkab/AlamofireNetworkActivityLogger
https://github.com/facebook/stetho

The aim of this project is to log the Alamofire request and response to the Safari Web Inspector. By console log method in javascript, header and body is logged in console tab.

Console Log : Header
Console Warn: Body
Console Error:Error

Import the library:

```swift
import AlamofireSafariLogger
```

Add the following code to `AppDelegate.swift application:didFinishLaunchingWithOptions:`:

```swift
AlamofireSafariLogger.shared.startLogging()
```

### Open Safari , enable developer menu.
![Open Debugger](https://raw.githubusercontent.com/springwong/AlamofireSafariLogger/master/open_debugger.png)
* To log iOS Device, in your device , Setting > Safari > Advanced > enable "Web Inspector"

### Open web inspector in developer menu when your app is running.

![Example Image](https://raw.githubusercontent.com/springwong/AlamofireSafariLogger/master/example.png)

### !!!Remember to prevent library's execution in your production app, i.e.

```ruby
#if DEBUG
AlamofireSafariLogger.shared.startLogging()
#endif
```

## Features
```swift
public var isGroupCollapse : Bool = true
public var isLogRequestHeader : Bool = true
public var isLogRequestBody : Bool = true
public var isLogResponseHeader : Bool = true
public var isLogResponseBody : Bool = true
public var isLogError : Bool = true
    
public var isDisableLog : Bool = false

```
Not Support multipart/form-data request body

## Installation

AlamofireSafariLogger is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'AlamofireSafariLogger'
```

## Author

rudolphwong2002@gmail.com

## License

AlamofireSafariLogger is available under the MIT license. See the LICENSE file for more info.
