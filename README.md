This is the buildsystem for the OpenWrt Linux distribution.

### 1. 安装git以下载OpenWrt源码。安装编译工具以进行交叉编译:

    sudo apt-get update
    sudo apt-get install git-core build-essential libssl-dev libncurses5-dev unzip gawk subversion mercurial gcc-multilib flex gettext

feeds中的部分软件包可能只能通过subversion (缩写: svn)或者mercurial下载源代码。如果你需要安装这些软件包，你同时也应当安装svn和mercurial:

sudo apt-get install subversion mercurial



### 2. 通过git来下载OpenWrt bleeding edge(trunk版本)：(参见Downloading Sources以获得更多选择):

git clone git://git.openwrt.org/openwrt.git

这将会创建'openwrt'这个目录。这个目录将会是OpenWrt的编译主目录。
OpenWrt的交叉编译工具链也已经被包含在内。

### 3. (可选)下载并安装所有可用的"feeds"(参见OpenWrt Feeds以获取更多选择):

    cd openwrt
    ./scripts/feeds update -a
    ./scripts/feeds install -a

### 4. 运行下面的命令(3选1!)让OpenWrt编译系统检查你的编译环境中缺失的软件包:

    make menuconfig  (推荐使用此命令)
    或者
    make defconfig
    或者
    make prereq
//如果以上3个命令都运行了,编译会出错! 


### 代码初步编译
    make -j8 V=s 



 

### 参考链接：

获取源码：
https://dev.openwrt.org/wiki/GetSource

Openwrt中文wiki网站
https://wiki.openwrt.org/zh-cn/start

Openwrt编译安装
https://wiki.openwrt.org/zh-cn/doc/howto/buildroot.exigence


