# XDA Thread

https://forum.xda-developers.com/xperia-xz2/development/aosp-aosp-8-1-h8266-t3843269

# Initialise the omnirom tree

  - In a terminal window, enter the following commands: 
```bash
mkdir sonyaosp_9.0
cd sonyaosp_9.0
repo init -u https://github.com/SonyAosp/platform_manifest -b android-9.0
```

  - Clone the local_manifests from GitHub using the following commands:
```bash
cd .repo
git clone https://github.com/MartinX3sAndroidDevelopment/sonyaosp_local_manifests.git local_manifests
cd ..
```

  - To download the code into the device repos created above, run the command:
```bash
repo sync -j$((`nproc`-1))
```

  - To build the image ("-userdebug" build)
```bash
. build/envsetup.sh;
lunch; # your device
make -j$((`nproc`-1));
```
