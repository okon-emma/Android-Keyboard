Keyboard For Android
==============================

This project is based on [AnySoftKeyboard](https://github.com/AnySoftKeyboard/AnySoftKeyboard)

====

Clone the repository

`git clone git://github.com/eyedol/kasahorow-Keyboard-For-Android.git`


After, you should have

```
.
|-- AndroidManifest.xml
|-- build
|-- build.gradle
|-- buildSrc
|-- dictionaries
|-- gradle
|-- gradlew
|-- gradlew.bat
|-- install_apk.sh
|-- keyboard_keystore
|-- proguard-rules.txt
|-- README.md
|-- res
|-- shippable.yml
|-- src
|-- StoreStuff
`-- temp_jni


```

### Debug Build

To make a debug  build, in the project's root directory, issue

`./gradlew assembleDebug`

This should build an unsigned apk for testing and debugging purposes.

### Release Build

To make a release build for distribution at the app store, make sure you have these files `local.signing.properties` and `local.extra.properties` in the root of the project.

**local.signing.properties**
```
STORE_FILE=signing_key_file
STORE_PASSWORD=store_password
KEY_ALIAS=key_alias
KEY_PASSWORD=key_password
```

A typical `local.signing.properties` content. Used the Android debug key details.
```
STORE_FILE=/home/username/.android/debug.keystore
STORE_PASSWORD=android
KEY_ALIAS=androiddebugkey
KEY_PASSWORD=android
```

**local.extra.properties**
```
CRASH_REPORT_EMAIL=crashreportemail@example.com
```

Then in the project's root directory, issue

`./gradlew assemble`
