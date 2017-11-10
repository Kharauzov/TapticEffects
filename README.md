# TapticEffects
Easily generate vibrations, built in Taptic Engine &amp; Haptic Feedback at your iOS apps.

![Swift](https://img.shields.io/badge/Swift-4.0-orange.svg)
![Platform](https://img.shields.io/badge/platform-iOS-lightgrey.svg)
[![License](https://img.shields.io/badge/license-mit-blue.svg)](https://doge.mit-license.org)

## Overview
TapticEffects generates feedback vibrations using Taptic or Haptic Engine on iOS device. I don't post any example project, becasue there is no need for this. Class is simple and easy in use. It is just wrapper of [UINotificationFeedbackGenerator](https://developer.apple.com/reference/uikit/uinotificationfeedbackgenerator), [UISelectionFeedbackGenerator](https://developer.apple.com/reference/uikit/uiselectionfeedbackgenerator), [UIImpactFeedbackGenerator](https://developer.apple.com/reference/uikit/uiimpactfeedbackgenerator).

## Usage

TapticEffects class doesn't require any initialization at your project. You can call its methods from any place using type methods of class. 

```swift
/// Performs haptic feedback - impact.
TapticEffectsService.performFeedbackImpact(style: .medium)

/// Performs haptic feedback - selection.
TapticEffectsService.performFeedbackSelection()

/// Performs taptic feedback based on 'TapticEngineFeedbackIdentifier'.
TapticEffectsService.performTapticFeedback(from: TapticEffectsService.TapticEngineFeedbackIdentifier.peek)

/// Available Identifiers

/// 'Peek' feedback (weak boom)
case peek = 1519
/// 'Pop' feedback (strong boom)
case pop = 1520
/// 'Cancelled' feedback (three sequential weak booms)
case cancelled = 1521
/// 'Try Again' feedback (week boom then strong boom)
case tryAgain = 1102
/// 'Failed' feedback (three sequential strong booms)
case failed = 1107

```

## Requirements
- Swift 3.0+
- iOS 10.0+ 
- iPhone 6s or higher

## Installation

### Manually
Just download and drop `TapticEffectsService.swift` class into your project.

## License
TapticEffects is available under the MIT license. See the LICENSE file for more info.

