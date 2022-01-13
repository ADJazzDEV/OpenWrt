注：
-
默认源为[Lede](https://github.com/coolsnowwolf/lede)，要换的需要在.github/workflows/build-openwrt.yml中换

openwrt-packages默认为[kenzok8](https://github.com/kenzok8/openwrt-packages)的源，要换的需要在diy-part1.sh中换

进入ssh后(黑屏按`Ctrl+C`)：

    cd openwrt
    make menuconfig
    
配置完成后`Ctrl+D`就不用管了

默认密码`password`
