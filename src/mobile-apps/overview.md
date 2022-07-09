# Mobile & Vendor Apps

## Project Setup

Tools:

1. Visual Studio Code or any other IDE
2. Android Studio
3. XCode version 12 or above.
4. Flutter 2.10
5. Android SDK

## usage

Run the following command in terminal:
```
flutter clean
flutter pub get
```

Navigate to ios folder in terminal:
```
cd ios
```

If you are using Apple M1 processor or later:
```
sudo arch -x86_64 gem install ffi
arch -x86_64 pod install
```

If you are using Apple Intel Processor:
```
pod install
```

## Routing

1. Navigator.push()
To switch to a new route, use the Navigator.push() method. The push() method adds a Route to the stack of routes managed by the Navigator. Where does the Route come from? You can create your own, or use a MaterialPageRoute, which is useful because it transitions to the new route using a platform-specific animation.


2. Navigator.pop()
How do you close the second route and return to the first? By using the Navigator.pop() method. The pop() method removes the current Route from the stack of routes managed by the Navigator.

## Testing

1. Connect a device or open emulator
2. Build the project
Run the following command in terminal:

if on android:
```
flutter build android
```

if on iOS:
```
flutter build ios
```

Run project
```
flutter run
```

## Build Signed APK

1. Make sure okaaik.jks file is present in android -> app folder
1. Make sure key.properties file is present in android folder
1. run flutter build apk --release in terminal
1. for app bundle run flutter build appbundle in terminal

## Build .ipa file for iOS

1. Right click on ios folder.
1. Select open in XCode.
1. Click on Product -> Archive.