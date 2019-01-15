### Buildroot for the SolidRun iMX8M based boards

This is a target platform for the iMX8M based SolidRun devices. It includes a custom config pre-configured to pull in the latest U-Boot and Linux kernel from the SolidRun BSP

### Building

The most basic image designed to boot from an SD-Card can be built with the following commands.

```
git clone https://github.com/SolidRun/buildroot.git --branch sr-latest
cd sr-latest
make solidrun_imx8mq_hbpulse_defconfig
make
```

### Flashing

Once the build completes the image can be found at `output/images/sdcard.img` and can written to the SD card with your favorite imaging utility or dd.

```
sudo dd if=output/images/sdcard.img of=/dev/sdX bs=4M conv=fsync
```
