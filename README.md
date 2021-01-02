# KSK-3022BT-FR-
Android "key layout" &amp; "key character map" files for KeySonic KSK-3022BT (FR) Keyboard.

# How to install

- In your android device, allow adb to be root (see *root access* in *developer options* of Lineage OS).
- On your computer:

cd C:\Users\<user>\AppData\Local\Android\Sdk\platform-tools

``````
adb root
adb kill-server (if adb root doesn't respond)
adb shell whoami (you should be root)
adb shell mount -o rw,remount /system
adb push Vendor_04e8_Product_7021_Version_0001.kl /system/usr/keylayout/Vendor_04e8_Product_7021_Version_0001.kl
adb push Vendor_04e8_Product_7021_Version_0001.kcm /system/usr/keychars/Vendor_04e8_Product_7021_Version_0001.kcm
adb shell reboot
``````

- After the reboot of the android device, press a few keys to wake-up the keyboard.
- On your computer:

``````
adb shell dumpsys input
``````
 you should see something like this:
 
 ``````
     10: Bluetooth 3.0 Keyboard
      Classes: 0x80000003
      Path: /dev/input/event10
      Descriptor: 799f05d8f2a5405762e7de4263dc28de03fcdafe
      Location:
      ControllerNumber: 0
      UniqueId: 43:9E:93:00:73:20
      Identifier: bus=0x0005, vendor=0x04e8, product=0x7021, version=0x0001
      KeyLayoutFile: /system/usr/keylayout/Vendor_04e8_Product_7021_Version_0001.kl
      KeyCharacterMapFile: /system/usr/keychars/Vendor_04e8_Product_7021_Version_0001.kcm
      ConfigurationFile:
      HaveKeyboardLayoutOverlay: false
``````      
