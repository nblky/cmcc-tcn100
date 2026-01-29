# CMCC-TCN100 飞牛安装说明

感谢各位大佬无私奉献！！！

黄鱼上车请认准头像。

买前请三思，不买立省！！

## 镜像烧录说明 

### 镜像烧录：

​	镜像采用 （[GitHub - ophub/fnnas](https://github.com/ophub/fnnas)）仓库代码自行编译或者下该大佬打包好的镜像（rock-5c），直接进行dtb替换（armbianEnv.txt记得修改）。

### dtb编译：

​	重新适配dtb，我采用的是[GitHub - unifreq/linux-6.12.y](https://github.com/unifreq/linux-6.12.y)该大佬内核仓库，把dts放到对应路径修改编译并配上[rk35xx启用GPU加速解码，这算是启用了吗？ · Issue #213 · ophub/fnnas](https://github.com/ophub/fnnas/issues/213)该楼主提供的相关dts进行dtb编译，新生成直接替换就行。

U-boot 采用 rock5c的就可以了

## 目前使用情况与问题：

1.网卡、无线网卡 正常使用，有线千兆能跑满

 2.风扇正常调用，待优化 

3.led灯未完全适配

 4.关机异常：命令关机 会自己开机，

 5.av1 解码异常，其他测试解码 飞牛影视解码 没jellyfin解码强 

6.影视解码播放初av1， 有的正常解码着会卡住

 7.红外、蓝牙、遥控器没弄



## 使用技巧

通电后 串口进入uboot后 输入

```shell
ums 0 mmc 0 
```

将tcn100设备的蓝色usb口子与电脑相连，就能把设备上的emmc 像u盘一样挂到电脑上。方便dtb替换测试。