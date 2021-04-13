# R720-15IKBN-opencore

**该项目现在荒废停更，有缘再见。如有需要，推荐前往项目[happylzyy/Hackintosh-Lenovo-R720](https://github.com/happylzyy/Hackintosh-Lenovo-R720)**

## 前言
一开始只想用用大佬们弄好的 EFI 玩玩黑苹果，结果下载回来的 opencore efi 都不知道为什么用不了，我找的无一例外的都出现错误。后来看了B站up主@司波图的 opencore 制作演示，我也就想着跟着试着做了这么个EFI。当然这个EFI现在还存在着问题，我也花太多时间在这个EFI上了，已经有点心有余力不足了，现在发布出来希望路过的大佬们能伸出援手来完善这个EFI。

## 配置
|   类型   |   参数   |
|:--------|:--------|
|产品品牌  |联想|
|产品型号  |R720-15IKBN|
|CPU      |I5-7300HQ|
|核心显卡  |HD630|
|内存      |16G（自带SK Hynix HMA81GS6AFR8N-UH 8G + 自加 TEAMGROUP-SD4-2400 8G）|
|独立显卡  |GTX1050 2G（屏蔽）| 
|声卡     |Realtek ALC233|
|网卡     |Realtek 8821AE Wireless LAN 802.11ac PCI-E NIC|

## 更新记录
> 2020.10.12 ：
> 
> + 去除不必要的启动项；
> + 更新`opencore`到`0.6.2`；
> + 更新`kext驱动`；
> + 添加了`SMCBatteryMnager.kext`驱动，状态栏显示电池图标。
> + 之前问题依旧存在。

## 驱动情况
+ CPU 在 Intel power gadget 显示频率正常。
+ 内存显示 16G 使用正常。
+ 声卡通过注入 `alcid=28` ，可以使用。
+ 核心显卡识别，但是显存只显示7MB，无法硬解。
+ 独立显卡屏蔽
+ 有线网络正常。
+ 无线网络未驱动，貌似无法驱动，需要使用wifi的可以考虑更换受支持的网卡或者使用外置网卡。
+ 蓝牙未驱动。
+ 使用`MacBookPro14,3`作为SMBios型号，三码使用[GenSMBios](https://github.com/corpnewt/GenSMBIOS)生成，推荐自行生成三码。
+ 未定制USB接口。

----
+ 本项目基本按照[Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)流程设置引导。
+ 途中可能因解决问题加入了一些可能不需要的文件或设置，所以该EFI不为最精简的EFI。
