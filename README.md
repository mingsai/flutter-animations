# Flutter Animations Cheat Sheet
[![Codemagic build status](https://api.codemagic.io/apps/5d360a1b3b905a001cfaa874/5d360a1b3b905a001cfaa873/status_badge.svg)](https://codemagic.io/apps/5d360a1b3b905a001cfaa874/5d360a1b3b905a001cfaa873/latest_build)

*WIP*

List of animations and transitions that you can used in Flutter.

Available as a [webpage](https://flutter-animations-cheat-sheet.codemagic.app/#/).

# Building
Last tested version of Flutter that works with this repo is `1.10.14`:
  * **Important**: Use `version` otherwise desktop won't be picked up: `1.10.14`

## Building for Web
Upgrade flutter to minimum `1.10.14`, enable web compilation and run:
```
flutter version 1.10.14
flutter config --enable-web
flutter run -d chrome -v
```

## Building for Desktop
Enable desktop builds by running in the terminal:
```
flutter config --enable-linux-desktop --enable-macos-desktop --enable-windows-desktop
```
### Linux
- Add the following to `.bash_profile` but replace `$HOME/flutter/` with path to your Flutter folder
```
# Add Flutter
export PATH="$PATH:$HOME/flutter/bin"
# Add Dart
export PATH="$PATH:$HOME/flutter/bin/cache/dart-sdk/bin"
```
### Mac
- Add the following to `.bash_profile` but replace `$HOME/flutter/` with path to your Flutter folder
```
# Add Flutter
export PATH="$PATH:$HOME/flutter/bin"
# Add Dart
export PATH="$PATH:$HOME/flutter/bin/cache/dart-sdk/bin"
```
- Update CocoaPods:
```
brew upgrade cocoapods
pod setup
gem install cocoapods
```
### Windows
- Install Visual Studio Community 2019 with [Desktop development with C++](https://devblogs.microsoft.com/cppblog/windows-desktop-development-with-c-in-visual-studio/#installation). 
Make sure that those components are installed:
* `MSVC v142 - VS 2019 C++ x64/x86 build tools (v14.23)`	
* `Windows 10 SDK (10.0.17763.0)` 

## Running on Desktop
Enter `flutter-animations` in your terminal and run `flutter run`. 
You might need to use `-d` to pick desktop if you have any other device connected.

OR

Open in your ide `flutter-animations` 
In IntelliJ/VS Code select appropriate device via device picker and run tha app

# Running Flutter Driver tests on Desktop
### Windows
```
flutter packages get
dart .\lib\tests\test.dart -r 800x800
```

### MacOs/Linux
```
flutter packages get
dart ./lib/tests/test.dart -r 800x800
```