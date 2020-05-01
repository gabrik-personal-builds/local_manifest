# Local Manifest for Xiaomi Redmi4A (rolex) build


## How to build

Initialize repo
```
repo init -u git://github.com/LineageOS/android.git -b lineage-17.1
```
Add local manifest
```
git clone https://github.com/gabrik-personal-builds/local_manifest .repo/local_manifests -b master
```

Sync


```
repo sync -c --force-sync --no-clone-bundle --no-tags -j$(nproc --all)
```

Prepare environment

```
$ source build/envsetup.sh
$ export _JAVA_OPTIONS="-Xmx8g"
$ ccache -M 50G
$ breakfast lineage_rolex-userdebug
$ mka j$(nproc --all) bacon
```