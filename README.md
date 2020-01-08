# openwrt18.06
编译命令如下:

1. 首先装好 Ubuntu 64bit，推荐  Ubuntu  19  LTS x64
http://releases.ubuntu.com/19.10/ubuntu-19.10-desktop-amd64.iso

2. 命令行输入 sudo apt-get update ，然后输入
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler

3.    git clone https://github.com/Leo-Jo-My/openwrt18.06   ####命令下载好源代码，然后 cd  openwrt18.06 进入目录

4.     ./scripts/feeds update -a && ./scripts/feeds install -a    ####更新FEEDS

5.      make menuconfig   最后选好你要的路由  

6.输入   make  V=99  开始编译  

####默认登陆IP 192.168.1.1, 密码 password

This is the buildsystem for the OpenWrt Linux distribution.

To build your own firmware you need a Linux, BSD or MacOSX system (case
sensitive filesystem required). Cygwin is unsupported because of the lack
of a case sensitive file system.

You need gcc, binutils, bzip2, flex, python3.5+, perl, make, find, grep, diff,
unzip, gawk, getopt, subversion, libz-dev and libc headers installed.

1. Run "./scripts/feeds update -a" to obtain all the latest package definitions
defined in feeds.conf / feeds.conf.default

2. Run "./scripts/feeds install -a" to install symlinks for all obtained
packages into package/feeds/

3. Run "make menuconfig" to select your preferred configuration for the
toolchain, target system & firmware packages.

4. Run "make" to build your firmware. This will download all sources, build
the cross-compile toolchain and then cross-compile the Linux kernel & all
chosen applications for your target system.

Sunshine!
	Your OpenWrt Community
	http://www.openwrt.org


