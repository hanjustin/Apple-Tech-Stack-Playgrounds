WIP

WIP

# Table of Contents

* Objective-C
* Swift
    * Property Wrappers
        * Projected value & Wrapped value
    * Structured Concurrency
        * `Task` & `TaskGroup`
    * Actors
        * `@MainActor` for main thread
    * Swift Macros
        * Uses SwiftSyntax behind to add code at compile time
* Foundation
    * ARC & Autorelease Pool
        * Manual reference counting -> error prone
        * `-retain`, `-release`, `-autorelease` added by compilers
    * Concurrency
        * GCD & NSOperationQueue
        * UI Main thread
        * Race condition
        * Deadlock
    * KVO & Notification
    * IPC & XPC
    * Data Persistance
        * UserDefaults (plist)
            * Cleared after uninstall
        * Core Data & SQLite
        * Keychain
            * Persists even after uninstall
        * iCloud

* UIKit
    * Data flow
        * MVC
        * Delegate pattern
        * Class Views
* SwiftUI
    * Data flow
        * MVVM
        * State & Property Wrappers
            * @State, @ObservedObject, @EnvironmentObject
        * Struct Views
* Core Data & SwiftData


## Objective-C

### Classes
`MyClass.m` class extensions for private properties and methods
`MyClass.h` for public properties and methods

`-` for instance methods
`+` for class methods

**Init**

```
- (instancetype)init {
  self = [super init];
  if (self) {
    _num = 23;
  }
  return self;
}

id anObject = [[MyClass alloc] init];
```

### Properties
Auto-syntehsize = Free getter, setter, and instance variable.

* Copy, weak, strong, readonly, readwrite, atomic, nonatomic

```
@interface MyClass : NSObject

@property float value;
@property (nonatomic, strong) NSString *text;

@end
```

### Delegate

Use `weak` to avoid strong reference cycle

### Literals

#### Compiler directives

* @class
* @interface
* @implementation
* @end
* @protocol
* @required
* @property
* @synthesize
* @dynamic

* @throw
* @try
* @catch
* @finally

* @selector
* @autoreleasepool
* @import

* @[]
* @{}
* @10 - `NSNumber`
* @"Hello" - `NSString`

#### Constants

```
static NSString * const HTTPMethodGET = @"GET";
static const CGFloat ButtonHeight = 100.0;

NSArray *brands = @[@"toyota", @"ford", @"honda"];
```



