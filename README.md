# TWRP device tree for OnePlus 13

OnePlus 13 (codenamed _"dodge"_) is a high-end smartphone from OnePlus.

## Build it yourself?

```
mkdir twrp && cd twrp
repo init --depth=1 -u https://github.com/TWRP-Test/platform_manifest_twrp_aosp.git -b twrp-16.0
repo sync
git clone --depth=1 https://github.com/WenHao-Dev/twrp_device_oneplus_dodge device/oneplus/dodge
```

```
source build/envsetup.sh
lunch twrp_dodge-bp2a-eng
make recoveryimage
```

If there is no error, recovery.img will be found in out/target/product/dodge/recovery.img

**NOTE**

Using Github Actions to build `twrp-16` branch may fail because of the large source

## Features

Works:
- [X] ADB
- [X] Display
- [X] Decryption
- [X] Fasbootd
- [X] Flashing
- [X] MTP
- [X] Sideload
- [X] USB OTG
- [X] Vibrator
- [X] Mount /data
- [X] Touch

## To use it:

```
fastboot flash recovery recovery.img
```

or

```
fastboot flash recovery_a recovery.img
fastboot flash recovery_b recovery.img
```
