                    ubuntu16.04 蓝牙不能使用的情况
question：蓝牙缺少重要组件
solve：
1.在虚拟机中安装windows系统，从c:\windows\system32\drivers中找到.hex文件，然后用hex2hcd工具将.hex 改为 BCD.hcd
2.将BCM.hcd移动到相应的文件夹
$mv ./BCM.hcd /lib/firmware/brcm

如果不能用使用,反复一下两个命令，然后再打开蓝牙
rfkill unblock bluetooth
rfkill block bluetooth
