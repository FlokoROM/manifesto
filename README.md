![FlokoROM](https://lindwurm.neocities.org/img/floko/flokowall_v4_mini.png)

# How to build

## Basic

Read:

* [AOSP Guide](https://source.android.com/setup/build/requirements)
* [LineageOS wiki](https://wiki.lineageos.org/devices/guacamoleb/build)
* optional: [Japanese Guide](https://dev.maud.io/entry/2019/07/18/howto-build-lineageos-16-0/)

## Download the sources

Initialize repo:

```sh
repo init -u https://github.com/FlokoROM/manifesto.git -b 11.0
```

Sync(Download):

```sh
repo sync -j32 -c --no-clone-bundle --no-tags
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

## I want to make my build as OFFICIAL

Great. Please read this article and send PM: https://github.com/FlokoROM/manifesto/wiki/How-to-official
