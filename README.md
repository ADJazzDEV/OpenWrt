注意：
-
默认源为lede，要换需要在.github/workflows/build-openwrt.yml中换

openwrt-packages为kenzok8的源，要换需要在diy-part1.sh中换

具体安装方法(大概流程)：
-
SSH connection to Actions 改为 true

进入ssh后：

    cd openwrt
    make menuconfig
