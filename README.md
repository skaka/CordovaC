# CordovaC
easy to combiler project cordova (Script shell) combiler and run on mobile for easy

this script put in "/usr/bin/runapp" and give it permit "chmod 755 runapp"


================================================

#!/bin/sh
cordova requirements
cordova build android
adb install -r -t 'platforms/android/app/build/outputs/apk/debug/app-debug.apk'
name=$(grep -oP '(?<=id=").*?(?=\" version)' config.xml)
adb shell am start "$name/.MainActivity"

====================================================



Thank you
