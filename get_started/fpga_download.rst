FPGA码流烧录
=================================================

.. attention:: 下载码流需要先保证驱动安装成功


1. 打开TD软件，选择 *download*

    .. figure:: http://odfef978i.bkt.clouddn.com/E203_TD_download.png
        :width: 600px
        :align: center

#. 添加 bitstream文件，选择 `LicheeTangNewIoMap\_BitStream.bit <https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/LicheeTangNewIoMap_BitStream.bit>`_

    .. figure:: http://odfef978i.bkt.clouddn.com/E203_TD_add.png
        :width: 600px
        :align: center

#. 如果 Mode 为 *JTAG*，断电后则恢复默认，所以为了上电自动启动，需要选择 **PROGRAM FLASH** 。（时间较长）
#. 如果需要进行IO修改，或者功能修改，请使用源码自行进行修改。`e203mini_new.tar.gz <https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/e203mini_new.tar.gz>`_






