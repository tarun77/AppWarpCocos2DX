##Cocos2DX SDK for AppWarp

Visit [AppWarp Cocos2DX home page](https://github.com/shephertz/AppWarpDeveloper/wiki/Cocos2DX-Home) to learn about AppWarp features and documentation.
##Instructions for iOS

* Download the contents of this repo

* Extract the contents and add (drag n drop) the AppWarpX folder to your xcode project.

* Your XCode structure should look something like this

![AppWarp Cocos2dx iOS](https://dl.dropboxusercontent.com/u/61084350/xcode_cocos2dx.png)

* Build

##Instructions for Android

* Download the contents of this repo

* Extract and add the AppWarpX folder next to your Classes folder. The directory structure should look like this

![AppWarp Cocos2dx iOS](https://dl.dropboxusercontent.com/u/61084350/android_cocos2dx.png)

* Edit proj.android\jni\Android.mk file

Add AppWarp source c and cpp files so that they are built. For example something like this

```
LOCAL_SRC_FILES := hellocpp/main.cpp \
                   ../../Classes/AppDelegate.cpp \
                   ../../Classes/HelloWorldScene.cpp \
                   ../../AppWarpX/appwarp.cpp \
                   ../../AppWarpX/appwarp_extended.cpp \
                   ../../AppWarpX/base64.cpp \
                   ../../AppWarpX/cJSON.c \
                   ../../AppWarpX/HMAC_SHA1.cpp \
                   ../../AppWarpX/requests.cpp \
                   ../../AppWarpX/SHA1.cpp \
                   ../../AppWarpX/socket.cpp \
                   ../../AppWarpX/urlencode.cpp \
                   ../../AppWarpX/utilities.cpp
```

Also add the following at the end of your Android.mk file for curl

```
$(call import-module,cocos2dx/platform/third_party/android/prebuilt/libcurl)
```
* Build the native code

* Add the following to your manifest file

```
<uses-permission android:name="android.permission.INTERNET" />
```

* Run your Android application
