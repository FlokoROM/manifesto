# FlokoROM

## Basic

Read:

* [AOSP Guide](https://source.android.com/setup/build/requirements)
* [LineageOS wiki](https://wiki.lineageos.org/devices/cheeseburger/build)
* optional: [Japanese Guide](https://dev.maud.io/entry/2018/03/19/howto-build-lineageos-15-1/)

## Download the sources

Initialize repo:

```sh
repo init -u https://github.com/FlokoROM/manifesto.git -b p9.0
```

Sync(Download):

```sh
repo sync -j8 -f --no-clone-bundle --no-tags
```

## Build

```sh
export ALLOW_MISSING_DEPENDENCIES=true
```

```sh
. build/envsetup.sh
```

```sh
brunch <device> 2>&1 | tee ~/log/floko_$(date '+%Y%m%d_%H-%M-%S').log
```
