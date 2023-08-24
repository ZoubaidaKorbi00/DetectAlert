# DetectAlert
This Kotlin module can be used to detect if an Android device has root access. It checks for common binaries, files, and permissions that indicate root access.
# Usage
To use the root detection module in your Android app:
1.Include the module in your project dependencies
``` Groovy 
implementation 'com.example.rootdetection:root-alert:1.0'
```
2. Instantiate the RootAlert class
``` kotlin 
val rootChecker = RootAlert()
```
3. Call the isRooted() method to check if the device is rooted
``` kotlin
if (rootChecker.isDeviceRooted()) {
  // Device is rooted
} else {
  // Device is not rooted 
}
```
# Implementation
The RootAlert class checks for the following indicators of root access:

Common root binaries like su, busybox, etc.
Presence of common root folders like /system/bin/, /system/xbin/, etc.
Write access to /system folder
Root permissions like com.noshufou.android.su, eu.chainfire.supersu etc.
The class combines all these checks to determine if root access is available or not.


