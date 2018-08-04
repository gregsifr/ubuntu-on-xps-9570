**DISCLAIMER: Use at your own risk. These instructions could cause data loss, damage to your system, or result in your system becoming unusable.**


## Table of Contents

Power Saving options:
* [Keep Bluetooth off by default during startup](#set-bluetooth-off-as-default)
* Wifi/Bluetooth power saving modes
* Turn off / disable touchscreen
* Disable nVidia powerdraw (consumes around 7w when idle)
* Enable NVME APST (allows NVME SSDs to be switched to lower power states when idle)
* Enable power saving features for the i915 kernel module
* Undervolt CPU and iGPU

Usability options:
* Enable touchpad gestures using libinput.




###### Set Bluetooth off as default

As per [this Ask Ubuntu answer](https://askubuntu.com/a/1047455/434826), the solution is to edit `/etc/default/tlp`.

Specifically find and change:
```bash
# Radio devices to disable on startup: bluetooth, wifi, wwan.
# Separate multiple devices with spaces.
#DEVICES_TO_DISABLE_ON_STARTUP="bluetooth wifi wwan"
```

To read:
```bash
DEVICES_TO_DISABLE_ON_STARTUP="bluetooth"
```

