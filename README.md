# Device Tree Asus ZenFone 6 (ASUS_I01WD)

The Asus ZenFone 6 (codenamed _"ASUS_I01WD"_) is a smartphone from Asus.
It was released in May 2019.

## Compile

First download twrp 12.1 tree:

```
repo init -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
```

Now you can sync your source:

```
repo sync
```

To auotomatic make the twrp installer, See https://gerrit.twrp.me/c/android_build/+/4964 for details

Finally execute these:

```
. build/envsetup.sh
export ALLOW_MISSING_DEPENDENCIES=true
export LC_ALL=C
lunch twrp_I01WD-eng
mka bootimage
```

To test it:

```
fastboot boot out/target/product/I01WD/boot.img
```

Kernel Source: https://github.com/asus-development/android_kernel_asus_sm8150/tree/android-11-twrp
