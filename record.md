 #  aplexOS
 ## 1. 如果需要急需处理U-Boot和Linux Kernel编译问题，请参考下面编译方式，注意修改编译器前缀：
 ###       1. U-Boot编译：
            1. make mx6dlsabresd_config CROSS_COMPILE=arm-linux-gnueabihf- ARCH=arm
            2. make CROSS_COMPILE=arm-linux-gnueabihf- ARCH=arm
            3. 输出文件：
                1. u-boot.imx                                  ---->     u-boot-imx6dlsabresd_sd.imx
###        2. Linux Kernel编译：
            1. 配置编译：make imx_v7_android_defconfig ARCH=arm
            2. 内核编译：make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- LOADADDR=0x10008000 zImage
            3. 设备树编译：make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- LOADADDR=0x10008000 dtbs
            4. 输出文件：
                1. arch/arm/boot/zImage             ---->       zImage
                2. arch/arm/boot/dts/imx6dl-sabresd.dtb     ---->       zImage-imx6dl-sabresd.dtb
