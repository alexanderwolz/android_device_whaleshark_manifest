# Repository Collection for Whale Shark AAOS

![GitHub release (latest by date)](https://img.shields.io/github/v/release/alexanderwolz/android_device_whaleshark_manifest)
![GitHub](https://img.shields.io/github/license/alexanderwolz/android_device_whaleshark_manifest)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/alexanderwolz/android_device_whaleshark_manifest)
![GitHub all releases](https://img.shields.io/github/downloads/alexanderwolz/android_device_whaleshark_manifest/total?color=informational)

## 🧑‍💻 About

This repository contains the local manifest definition for Whale Shark AAOS.

## 🛠️ Setup

This product is currently being tested against *TQ3A.230901.001.B1* (android-13.0.0_r76)

See [Android tags](https://source.android.com/docs/setup/about/build-numbers) for other build ids and branches

### Download AOSP repository and manifest

Clone this repository into the *.repo/local_manifest* folder of your AOSP root, such as:

1. ```cd $AOSP_HOME``` (this is a placeholder for your workdir)
1. ```repo init -u https://android.googlesource.com/platform/manifest -b android-13.0.0_r76```
2. ```git clone https://github.com/alexanderwolz/android_device_whaleshark_manifest.git -b android-13 .repo/local_manifests```
3. ```repo sync -c -j$(nproc --all)```

In any case there are several local manifests, clone repo somewhere else and symlink the ```whaleshark.xml``` directly.

## ⚙️ Build the product

This follows the normal AOSP build approach, e.g.
1. ```cd $AOSP_HOME```
1. ```source build/envsetup.sh```
2. ```lunch``` (choose your device)
4. ```m -j$(nproc --all)```
6. See compiled files at ```$ANDROID_PRODUCT_OUT``` (should be ```out/target/product/```)
