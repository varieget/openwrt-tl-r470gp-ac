# TL-R470GP-AC Ver5.0

适用于 TL-R470GP-AC Ver5.0 的 OpenWrt 19.07 版本

## 刷入步骤

0. 通过编程器备份 flash

1. 自行寻找使能 telnet 或 ssh 的方法

2. 通过 mtd 刷入 u-boot 可在 [这里下载](https://github.com/varieget/uboot-mt7621/actions)

   也可以选择自行编译，下面是需要注意的参数。

   ```
   Parse flash type: NOR
   set partition table: 192k(u-boot),64k(factory),-(firmware)
   set kernel offset: 0x40000
   set reset button pin: 8
   set system led pin: 15
   set CPU frequency: 880 MHz
   set DRAM frequency: 1200 MT/s
   Parse DDR init parameters: DDR3-128MiB
   Set baud rate: 115200
   ```

3. 在 u-boot 页面，上传 `sysupgrade.bin` 稍等片刻
