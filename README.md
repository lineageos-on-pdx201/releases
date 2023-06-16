# LineageOS Downloads

### Requirements
The latest Android 12 firmware (59.2.A.0.463), an [unlocked bootloader](https://developer.sony.com/open-source/aosp-on-xperia-open-devices/get-started/unlock-bootloader) and USB debugging enabled.

The latest LineageOS [copy-partitions](https://mirrorbits.lineageos.org/tools/copy-partitions-20220613-signed.zip) package.

The latest LineageOS .zip package and recovery .img file for pdx201 available [here](https://github.com/lineageos-on-pdx201/releases/releases).

The latest version of [Google's platform-tools](https://developer.android.com/tools/releases/platform-tools?hl=en#downloads) and a computer.

The latest [Google Apps](https://androidfilehost.com/?fid=4279422670115734716) .zip package (Optional)

### Flash steps
Reboot to bootloader
```
adb reboot bootloader
```

Flash LineageOS recovery
```
fastboot flash recovery recovery.img
```

Reboot to recovery
```
fastboot reboot recovery
```

Sideload the copy-partitions .zip package (Apply Update -> Apply from ADB)
```
adb sideload copy-partitions-date-signed.zip
```

Do a factory reset (Factory Reset > Format data / factory reset)

Sideload the LineageOS .zip package (Apply Update -> Apply from ADB)
```
adb sideload lineage-packagename.zip
```

If you want to flash any add-on such as Google Apps, you can directly go to [Installing Add-Ons section](https://github.com/LineageOS-on-pdx201/releases/blob/main/README.md#installing-add-ons), otherwise you can reboot to System

### Installing Add-Ons
Sideload the Google Apps .zip package (Apply Update -> Apply from ADB)
```
adb sideload MindTheGapps-packagename.zip
```

Reboot to System

### Reporting bugs
Create an issue [here](https://github.com/lineageos-on-pdx201/releases/issues) with the LineageOS exact version and steps on how to reproduce.

Google Apps, Google Camera, Magisk and SafetyNet related bugs will be ignored and immediately closed !

### Copyrights
Your warranty is now voided and I am not responsible for any bricks or bootloop.

```
Copyright (C) 2023 The LineageOS Project
```
