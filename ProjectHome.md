A bash script utility that resigns the Android Package (APK) files (Android applications)  with different certificates.


## Sample Usage ##

Download file from: https://apk-resigner.googlecode.com/svn/trunk/signapk.sh

**Parameters of the signapk.sh**

_param1:_ APK file, to be signed

_param2:_ keystore location

_param3:_ keystore pass

_param4:_ key alias

Signs the APK with the given new key


**Tutorial 1: Signing a stock application with your own android debug key**

Android Calculator Application, "com.android.calculator2" calculator.apk
```
./signapk.sh calculator.apk ~/.android/debug.keystore android androiddebugkey
```

It creates signed\_calculator.apk at the same path

**Tutorial 2: Default is your own debug key**
If you do not provide any key-related parameters (param2,param3 and param4), it uses your own android debug key as a default option.
```
./signapk.sh calculator.apk 
```

is same as above usage

For more information about signing your application; http://developer.android.com/tools/publishing/app-signing.html#debugmode
