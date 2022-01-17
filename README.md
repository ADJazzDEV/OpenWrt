### 目前使用SSH编译有问题，使用配置文件进行编译

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

### 本地编译：
系统：`Ubuntu 20.04` 

命令：
`apt-get update && apt-get -y install build-essential asciidoc binutils bzip2 curl gawk gettext git libncurses5-dev libz-dev patch python3.5 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf rsync`

`git clone -b main --single-branch https://github.com/Lienol/openwrt openwrt && cd openwrt`

`./scripts/feeds clean && ./scripts/feeds update -a && ./scripts/feeds install -a`

`make menuconfig`

`make -j8 download V=s`

`make -j1 V=s` (在非Root下编译)

编译完成后输出路径：openwrt/bin/targets
