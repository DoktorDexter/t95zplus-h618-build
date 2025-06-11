# Compile steps

- You need a Linux system environment with Docker installed
- Clone the Armbian repository to your local computer
'''
git clone https://github.com/LYU4662/h618-build.git
'''
- Copy all files in this repository to your local h618-build code directory (except t95zplus_android_dtb_dump.dts)
- The most important thing is to modify the VERSION file of h618-build, and change the 24.5.0-trunk in it to the latest file system version. The latest version in june 2025 is 25.8.0-trunk
- You must use a `non-root user` to execute the `build.sh` script and select the model to start compiling.
 - Modify kernel config to add AIC8800 WIFI driver support -> Device Drivers -> Network device support (NETDEVICES [=y]) -> Wireless LAN (WLAN [=y]) -> AIC wireless Support (AIC_WLAN_SUPPORT [=y]) -> AIC8800 bluetooth Support (AIC8800_BTLPM_SUPPORT [=y])
- The first compilation usually takes a long time, so you need to be patient.

# Reference & Thanks

https://github.com/NickAlilovic/build.git

https://github.com/cm9vdA/build-armbian.git