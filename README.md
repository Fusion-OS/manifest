<div align="center">

<img src="https://raw.githubusercontent.com/Fusion-OS/documentation/main/assets/banner/fuse-banner.png" >

</div>

A glimpse of of the project
---------------
Yet another minimalist aftermarket rom with some customisation and optimisations provide a clean and smooth android experience.

Requirements
------------
- At least 200G free disk space.
- A computer/server with at least 16GB RAM running Linux and preferably a fast and stable internet connection.
- Some basic knowledge of Linux commands, device tree management and git.

Instructions
------------
### Prerequisites
A properly configured build environment is required to build AOSP custom roms. A guide for setting up the build environment can be found [here](https://source.android.com/setup/build/initializing).

### Sync the source
```bash
        repo init -u https://github.com/Fusion-OS/manifest -b fourteen
        repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j$(nproc --all)

```

### Build
```bash
        source build/envsetup.sh
        lunch fuse_$device-userdebug
        make fuse-prod -j$(nproc --all) | tee log.log
```

Optional Flags
--------------
### Including GAPPS
```bash
WITH_GAPPS := true
```

Credits
-------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**AOSPA**](https://github.com/AOSPA)
 * [**HentaiOS**](https://github.com/hentaios)
 * [**Paranoid Android**](https://github.com/AOSPA)
 * [**Project Radiant**](https://github.com/ProjectRadiant)
 * [**StormbreakerOSS**](https://github.com/StormbreakerOSS)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**StyxOS**](https://github.com/stxyproject)
 * [**Pixel Experience**](https://github.com/PixelExperience)
 * [**PixelOS-AOSP**](https://github.com/PixelOS-AOSP)
 * [**StatixOS**](https://github.com/StatiXOS)
 * ... And the list never ends.