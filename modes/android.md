# Android



#### Links

* [Processing for Android](http://android.processing.org/)
* [Processing for Android Wiki @ github](https://github.com/processing/processing-android/wiki)
* [Android Processing Forum](https://forum.processing.org/one/android-processing.html)
* [Android Problems (Forum Topic)](https://forum.processing.org/one/topic/android-problems.html) - very useful, possibly dated. Says that `ANDROID_HOME` should point to sdk bin, but I'm not convinced.

##### Misc

* [Installing Android Studio on Mac OS X Yosemite](https://hrnn.github.io/2015/02/11/installing-android-studio-on-mac-os-x-yosemite/) - not sure if you need to set `STUDIO_JDK` - I didn't and no obvious problems.


##### Other Libraries

- [ke:tai](http://ketai.org/) this looks good!


## Installation

### Android SDK

Install Java and the Android SDK (installed with Android Studio).

Wiki says to make sure "Android SDK Platform-tools" and "Android 2.3.3 (API 10) SDK Platform" are installed and that version 10 is specifically required! Buy there is contradictory information since later on the Wiki it says only version 11 and above are supported!

But even with just API 23 (Android 6.0) I was able to run on Nexus 7.


### Processing

When I started Processing I had to specify the SDK path manually since `ANDROID_SDK` variable wasn't set! This sets values in `~/Library/Processing/preferences.txt`:

```
android.sdk.name=6.0
android.sdk.path=/Users/smathews/Library/Android/sdk
android.sdk.version=23
```

The sdk name/versions seem to be reset automatically if you change them manually. But check that.

An `AndroidManifest.xml` file is created along side the sketch. `minSdkVersion` and `targetSdkVersion` (assert tested and supported without compatibility mode) seem to be set automatically from preferences, but can be modified to support older Android systems. It seems any SDK version you specify here should have it's SDK Platform installed.


### Device

USB debugging is required I think.

Devices can randomly lose connection and upload can silently fail, so verify connection with `adb devices -l`.

## Using

In AndroidMode Processing menus are changed. Running with a device attached automatically runs on device (not sure what happens if no device attachd).

Wiki has notes about in/compatibilities.

Use `displayWidth` and `displayHeight` to target different screens.


## Emulator

Processing should create an AVD when it tries to launch sketch, but doesn't seem to work. 
