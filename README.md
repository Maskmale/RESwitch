# RESwitch

Open source alternative to `UISwitch`, customizable via `UIAppearance`.

![Screenshot of RESwitch](https://github.com/romaonthego/RESwitch/raw/master/Screenshot.png "RESwitch Screenshot")

## Requirements
* Xcode 4.5 or higher
* Apple LLVM compiler
* iOS 5.0 or higher
* ARC

## Demo

Build and run the `RESwitchExample` project in Xcode to see `RESwitch` in action.

## Installation

The recommended approach for installating RESwitch is via the [CocoaPods](http://cocoapods.org/) package manager, as it provides flexible dependency management and dead simple installation.

Install CocoaPods if not already available:

``` bash
$ [sudo] gem install cocoapods
$ pod setup
```

Edit your Podfile and add `RESwitch`:

``` bash
$ edit Podfile
platform :ios, '5.0'
pod 'RESwitch', '~> 1.0'
```

Install into your Xcode project:

``` bash
$ pod install
```

Add `#include "RESwitch.h"` to the top of classes that will use it.

## Example Usage

TO DO

## Customization

You can customize the appearance of all switches using the appearance proxy (`[RESwitch appearance]`), or just of a single switch.

Use the following properties and tasks to customize `RESwitch`:

``` objective-c
@property (strong, nonatomic) UIImage *backgroundImage;
@property (strong, nonatomic) UIImage *overlayImage;
@property (strong, nonatomic) UIImage *knobImage;
@property (strong, nonatomic) UIImage *highlightedKnobImage;
@property (assign, readwrite, nonatomic) CGSize knobOffset;
@property (assign, readwrite, nonatomic) CGSize textShadowOffset;
@property (strong, nonatomic) UIFont *font;

- (CGFloat)cornerRadius;
- (void)setCornerRadius:(CGFloat)radius;
- (void)setTextOffset:(CGSize)offset forLabel:(RESwitchLabel)label;
- (void)setTextColor:(UIColor *)color forLabel:(RESwitchLabel)label;
- (void)setTextShadowColor:(UIColor *)color forLabel:(RESwitchLabel)label;
- (void)setTitle:(NSString *)title forLabel:(RESwitchLabel)label;
```

For example, this is how default appearance of `RESwitch` is set:

``` objective-c
[[RESwitch appearance] setBackgroundImage:[UIImage imageNamed:@"RESwitch.bundle/Background"]];
[[RESwitch appearance] setOverlayImage:[UIImage imageNamed:@"RESwitch.bundle/Overlay"]];
[[RESwitch appearance] setKnobImage:[UIImage imageNamed:@"RESwitch.bundle/Knob"]];
[[RESwitch appearance] setHighlightedKnobImage:[UIImage imageNamed:@"RESwitch.bundle/Knob_Highlighted"]];
[[RESwitch appearance] setKnobOffset:CGSizeMake(4, -3)];
[[RESwitch appearance] setCornerRadius:14];
[[RESwitch appearance] setFont:[UIFont boldSystemFontOfSize:17]];
[[RESwitch appearance] setTextOffset:CGSizeMake(0, 0) forLabel:RESwitchLabelOn];
[[RESwitch appearance] setTextOffset:CGSizeMake(0, 0) forLabel:RESwitchLabelOff];
[[RESwitch appearance] setTextShadowOffset:CGSizeMake(0, -1)];
```

## Contact

Roman Efimov

- https://github.com/romaonthego
- https://twitter.com/romaonthego
- romefimov@gmail.com

## License

RESwitch is available under the MIT license.

Copyright © 2013 Roman Efimov.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
