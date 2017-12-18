# Kernel command line

## LVDS
console=ttymxc0,115200 root=/dev/mmcblk3p2 rootwait rw can0 video=mxcfb1:off video=mxcfb0:dev=ldb,if=RGB24,fbpix=RGB32,fbmem=12M
## HDMI
console=ttymxc0,115200 root=/dev/mmcblk3p2 rootwait rw can0 video=mxcfb0:off video=mxcfb1:dev=hdmi,1920x1080M@60,if=RGB24,bpp=16
