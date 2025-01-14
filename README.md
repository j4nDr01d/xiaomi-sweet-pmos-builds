# Nightly SM7150 PostmarketOS Builds

This repository contains workflows and configurations to automatically build PostmarketOS edge images for the [Xiaomi Redmi Note 10 Pro (xiaomi-sweet)](https://wiki.postmarketos.org/wiki/Xiaomi_Redmi_Note_10_Pro_(xiaomi-sweet)), one of the devices supported by [sm7150-mainline](https://github.com/sm7150-mainline). These images are intended for testing purposes only and should make testing more accessible to people without the capabilities to compile the kernel from source.

## Image Information

The CI builds images once per week on fridays at midnight UTC. When completed, it will upload the artifact that was built. These artifacts contain `boot-xiaomi-sweet.img` and an xz-compressed rootfs-xiaomi-sweet.img. Artifacts are kept for one week (i.e. until the next rebuild).

The default user is called `user`, the password is `147147`, just like on official PostmarketOS stable images.

## Downloading

Head to the [Actions tab](https://github.com/Kanishka-Developer/nightly-builds/actions), select the most recent successful run and download the artifact with the desired UI. Extract the zip, de-compress the rootfs and you're ready to flash!

`fastboot flash userdata rootfs-xiaomi-sweet.img`

`fastboot flash boot boot-xiaomi-sweet.img`