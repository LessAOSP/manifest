# MantleOS

 Getting Started
---------------
To get started with the MantleOS sources, you'll need to get
familiar with [Git and Repo](https://source.android.com/setup/build/downloading) and also check [System Requirements](https://source.android.com/docs/setup/start/requirements)

 To initialize your local repository, use command:

```bash
repo init -u https://github.com/MantleOS/manifest.git -b 15 --git-lfs
```

For saving space you can do shallow clone of repo init process

```bash
repo init -u https://github.com/MantleOS/manifest.git -b 15 --git-lfs --depth=1
```

Then sync up:
-J8 here is 8 threads, you can change based on your PC processor.

```bash
repo sync -c -j8
```

If you want to use all cores then use below command

```
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

Building the System
-------------------
 Initialize the ROM environment with the envsetup.sh script.

```bash
. build/envsetup.sh
```

Lunch your device after cloning all device sources if needed.
Note : lunch command will change based on device ex: lunch aosp_sea-ap2a-eng

```bash
lunch aosp_devicecodename-ap3a-buildtype
```

Start compilation

```bash
mka bacon
```

# Credits:

 * [**LineageOS**](https://github.com/LineageOS)