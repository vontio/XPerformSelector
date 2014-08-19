Trick to performSelector in swift
====

## Background

performSelector is hidden from swift,can't compile if use performSelector in swift.
But performSelector is valid in objective-c. With objc bridge,we can use performSelector now.

## quick usage

```
XPerformSelector.perform(self, selector: "test")
```

## don't know how to use objc in swift? read this first

[Swift and Objective-C in the Same Project](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/BuildingCocoaApps/MixandMatch.html)

## apis

```
+(void) perform: (id)target selector:(SEL)selector;
+(void) perform: (id)target selector:(SEL)selector count:(int)count, ...; 

+(void) perform: (id)target selector:(SEL)selector withObject:(id)arg1;
+(void) perform: (id)target selector:(SEL)selector withObject:(id)arg1 withObject:(id)arg2;

+(void) perform: (id)target selector:(SEL)selector afterDelay:(NSTimeInterval)delay;
+(void) perform: (id)target selector:(SEL)selector withObject:(id)arg1 afterDelay:(NSTimeInterval)delay;
```
