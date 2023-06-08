### 一、理论知识
- 黑苹果 (hackintosh)：在非苹果官方认可的设备上安装 macOS 的设备
- 白苹果 (macintosh)：苹果官方的设备 
### 二、硬件选择
- CPU: 选择主流十二代英特尔 CPU 
- GPU：选择 AMD 主流 GPU，5000 系/6000 系，大牌散热好即可
- 主板：一线主流品牌主板华硕等，BIOS 设置清晰容易，具有 CFG Lock 选项即可
- 内存：内存无要求，主流大牌即可
- 蓝牙&WiFi：博通免驱即可，英特尔无线网卡无法实现 apple 全部功能
- 固态硬盘：国产 m.2 固态硬盘，致态等
- 其他：根据喜好选择即可，大于 16G 的 U 盘
### 三、软件选择
- 镜像：[macOS Monterey](https://heipg.cn/tag/macos-monterey) / [macOS Big Sur](https://heipg.cn/tag/macos-big-sur) / [macOS Catalina 10.15](https://heipg.cn/tag/macos-catalina) / [macOS Mojave 10.14.6](https://heipg.cn/macos/macos-mojave-18g87-clover-r5050.html) / [macOS High Sierra 10.13.6](https://heipg.cn/macos/macos-high-sierra-10-13-clover-4606.html) / [macOS Sierra 10.12.6](https://heipg.cn/macos/macos-sierra-10-12-6-with-clover-4133.html) / [OS X El Capitan 10.11.6](https://heipg.cn/macos/os-x-el-capitan-10-11-6-15g31-clover-r3651-and-wepe.html)
- CloverEFI / OpenCore EFI：GitHub 上寻找与自己电脑主板 CPU 显卡型号相同即可
- 软件：balenaEtcher  transmac diskgenius EasyUEFI
[参考文章]([2023年黑苹果硬件配置推荐表-黑苹果星球 (heipg.cn)](https://heipg.cn/tutorial/diy-hackintosh-2020.html))
### 四、安装过程
- 1 从 github 或者其他网站选择适合自己的 EFI (引导 mac 的文件) 文件，镜像文件
- 2 使用 balenaEcher/transmac 将镜像文件烧录至 U 盘，并使用适合自己的 EFI 文件替换烧录的 EFI 文件
- 3 安装系统根据不同引导安装系统 (多次重启)，选择硬盘的不同分区并格式化为 APFS 格式。
[Clover 引导参考文章](https://blog.csdn.net/unreliable_narrator/article/details/64438619)
[OpenCore 引导参考文章](https://blog.csdn.net/weixin_44219473/article/details/119061501)
[OpenCore 引导参考文章](https://www.bilibili.com/video/BV1f541147Ag)
### 五、联想小新 chao 5000
[EFI 地址](https://github.com/masonsxu/Hackintosh-Lenovo-Chao5000)
[镜像地址macOS Catalina 10.15.2(19C57) Installer for Clover 5100 and WEPE](https://mirrors.dtops.co/ISO/MacOS/)
EFI 修改 ：将下载中的 BOOTX64. efi 和 CLOVERX64. efi 替换为镜像中的 BOOTX64. efi 和 CLOVERX64. efi 升级CLOVER
Config. list 修改 1：[This version of Mac OS X is not supported on this platform! ](https://blog.csdn.net/HiZhanYue/article/details/92762417)
Config. list 修改 2：[clover删除多余引导](https://blog.csdn.net/weixin_35935712/article/details/113029276)     [ Clover隐藏多余分区](https://blog.csdn.net/JoeBlackzqq/article/details/89892079)
最后将 clover 文件夹复制进 MSP 分区并使用 EasyUEFI 将 mac 引导加载进去即可 [使用EasyUEFI修改EFI分区引导启动项数据](https://www.mfpud.com/topics/198/)
全文参考链接：[主页 - 国光的黑苹果安装教程：手把手教你配置 OpenCore (sqlsec.com)](https://apple.sqlsec.com/)