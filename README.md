## 当前编译状态：
| 源码+版本 | 固件编译状态 | 脚本文件 | 固件下载 |
| :-------------: | :-------------: | :-------------: | :-------------: |
| [![](https://img.shields.io/badge/Lede-6.6-32C955.svg?logo=openwrt)](https://github.com/ranqingwen/OpenWrt_x64_2305/blob/main/.github/workflows/OpenWrt_x64.yml) | [![](https://github.com/ranqingwen/OpenWrt_x64_2305/actions/workflows/OpenWrt_x64.yml/badge.svg)](https://github.com/ranqingwen/OpenWrt_x64_2305/actions/workflows/OpenWrt_x64.yml) | [![](https://img.shields.io/badge/脚本-配置-orange.svg?logo=apache-spark)](https://github.com/ranqingwen/OpenWrt_x64_2305/tree/main/diy_script/lede_diy/x86) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/ranqingwen/OpenWrt_x64_2305/releases) |

</br>

## 项目说明 [![](https://github.com/gxnas/OpenWrt_Build_x64/blob/main/personal/describes.svg)](#项目说明-)
- 固件编译使用的源代码来自：[![Lean](https://img.shields.io/badge/Lede-Lean-red.svg?style=flat&logo=appveyor)](https://github.com/coolsnowwolf/lede) 
- 项目使用 Github Actions 拉取 [Lean](https://github.com/coolsnowwolf/lede) 的 `Openwrt-23.05（内核版本6.6）` 源码仓库进行云编译
-  本库编译的x86固件为squashfs格式（ext4 与squashfs 格式的区别： ext4 格式的rootfs 可以扩展磁盘空间大小，而squashfs 不能。 squashfs 格式的rootfs 可以使用重置功能（恢复出厂设置），而ext4 不能）；
-  默认的固件容量：Kernel=32M、rootfs=968M，请确保安装OpenWrt的硬盘空间至少要有1G以上；
-  文件名带有efi字样的固件支持Uefi和Legacy两种引导方式启动，文件名不含efi的固件仅支持Legacy传统引导方式启动；
-  虚拟机安装的，请确保文件名和路径没有中文或者特殊符号，否则转换文件时有可能转换不成功；
-  OpenWrt升级方法：下载好对应版本的.img.gz文件到电脑上，不需要解压，然后在你的OpenWrt菜单“系统-备份/升级”直接选择下载好的.img.gz文件上传，刷写固件；
-  ******最好不要跨大版本升级（比如1806升级到2305，或者6.1内核升级6.6），大版本更新建议采用全新安装方可获得最佳的体验******
- 🛑 默认的IP地址：192.168.23.250；
- 🛑 默认用户名：root，无密码；
- 🛑 如需要更改OpenWrt默认的IP，可以用root登录SSH下输入命令 vi /etc/config/network 修改文件；
- 🛑 SSH界面也可输入 openwrt 打开系统快捷命令菜单

==============================================
 OpenWrt 快捷命令菜单（Shortcut Command Menu）
==============================================
1.更改 LAN 口 IP 地址（Change LAN port IP address）<br>
2.更改管理员密码（Change administrator password）<br>
3.重置网络和切换默认主题（Reset network and Switch default theme）<br>
4.重启系统（Reboot）<br>
5.关闭系统（Shutdown）<br>
6.释放内存（Release memory）<br>
7.恢复出厂设置（Restore factory settings）<br>
0.退出本快捷菜单（Exit shortcut menu）<br>

----
- REPO_TOKEN密匙制作教程：https://git.io/jm.md
- 云编译需要 [在此](https://github.com/settings/tokens) 创建个```token```,勾选：```repo```, ```workflow```，保存所得的key
- 然后在此仓库```Settings```->```Secrets```中添加个名字为```GH_TOKEN```的Secret,填入token获得的key

- Telegram通知```Settings```->```Secrets```中添加名字为```TELEGRAM_TO```和```TELEGRAM_TOKEN```，值分别为BOT_USER _ID和BOT_TOKEN
- 企业微信机器人通知```Settings```->```Secrets```中添加个名字为```WEBHOOK_SEND_KEY```，值为企业微信机器人https://qyapi.weixin.qq.com/cgi-bin/webhook/send?key=后面的值
----
<a href="#readme">
<img src="https://github.com/ranqingwen/Lede25-autobuild/blob/main/personal/return.svg" title="返回顶部" align="right"/>
</a>
