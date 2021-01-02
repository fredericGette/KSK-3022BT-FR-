# KSK-3022BT-FR-
Android "key layout" &amp; "key character map" files for KeySonic KSK-3022BT (FR) Keyboard.

# Usage
cd C:\Users\<user>\AppData\Local\Android\Sdk\platform-tools
./adb shell dumpsys input
./adb root
./adb kill-server
./adb shell whoami
./adb shell mount -o rw,remount /system
./adb push Vendor_04e8_Product_7021_Version_0001.kcm /system/usr/keychars/Vendor_04e8_Product_7021_Version_0001.kcm
./adb push Vendor_04e8_Product_7021_Version_0001.kl /system/usr/keylayout/Vendor_04e8_Product_7021_Version_0001.kl