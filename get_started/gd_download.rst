GD32固件下载
=================================================

.. attention:: LicheeTang出厂已经默认烧录了固件，本文只针对固件更新或重新下载

1. 使用swd接口对板载的 GD32F150 芯片进行烧录，写入 FPGA JTAG 的调试器固件。调试器固件可在 `anlogic-usbjtag <https://github.com/Lichee-Pi/anlogic-usbjtag>`_ 处下载，这里我们使用 `st-flash <https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/get_started/stlink-1.3.0-win64.zip>`_ 进行烧录。亦可使用 STVP 下载，但是注意看门狗启动一定要关掉，否则会导致芯片不断复位！

2. **焊接（或者用按着/调试夹子）** *swdio* 和 *swclk* 到 *stlink对应接口*。（位置参考前文引脚图）

3. 打开cmd命令行，进入 *st-flash\\bin* ，执行指令

    ``st-flash.exe write flash.bin 0x08000000``

烧录成功显示结果为:

.. figure:: http://odfef978i.bkt.clouddn.com/E203_download.png
  :width: 500px
  :align: center

  烧录成功-控制台输出示例

烧录成功后将LicheeTang插上电脑可以看到，在TD软件下载页面中也可以看到设备。如果没看到，请安装驱动，参照TD驱动安装

.. figure:: http://odfef978i.bkt.clouddn.com/E203_device.png
  :width: 250px
  :align: center

  设备管理界面
