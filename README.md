### 注：
默认源为[Lede](https://github.com/coolsnowwolf/lede)，要换的需要在.github/workflows/build-openwrt.yml中换

openwrt-packages默认为[ADJazz](https://github.com/ADJazzDEV/OpenWrt-package)的源，要换的需要在diy-part1.sh中换

.config文件为配置文件

SSH默认开启

进入ssh后(黑屏按`Ctrl+C`)：

    cd openwrt
    make menuconfig
    
配置完成后`Ctrl+D`就不用管了

默认密码`password`
