


## Load variables to build
export AOSP_TOPDIR=$(pwd)
export PATH=${AOSP_TOPDIR}/prebuilts/clang/host/linux-x86/clang-r445002/bin:$PATH
export PATH=${AOSP_TOPDIR}/prebuilts/gas/linux-x86:$PATH
export PATH=${AOSP_TOPDIR}/prebuilts/misc/linux-x86/lz4:$PATH
export ARCH=arm64
export CROSS_COMPILE=aarch64-linux-gnu-
export LLVM=1
~                                                         
## Load default config (if loaded, all the modifications will be lost)
make meson_defconfig

## Menu to modify kernel
make menuconfig
