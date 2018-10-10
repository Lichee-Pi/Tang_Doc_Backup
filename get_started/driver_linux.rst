Install TD driver on Linux
=================================================

#0. Insert LicheeTang into your computer and execute lsusb to see the information. Make sure USB VID:PID is 0547:1002 as shown in image below.

.. figure:: https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/get_started/237929105611360081.jpg
  :align: center

  Check for default linux driver.

#1. Set udev rules to enable LicheeTang to be accessed by the plugdev group

    Execute the following command in terminal to create a new udev rules file.

    .. code-block:: sh

        sudo nano /etc/udev/rules.d/91-anlogic-jtag.rules

    Copy the following code into text editor and save it, as shown in following image.

    .. code-block:: sh

        SUBSYSTEMS=="usb", ATTRS{idVendor}=="0547", ATTRS{idProduct}=="1002", \
          GROUP="plugdev", \
          MODE="0660"

.. figure:: https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/get_started/572316008299057820.jpg
  :align: center

  Create a new udev rule file.

Execute the following command in terminal to restart the udev service.

    .. code-block:: sh

        sudo service udev restart

#2. Open Tang Dynasty IDE.
    Go to ``<TD installation directory>/bin/`` and execute the following command to open TD IDE in GUI mode.

    .. code-block:: sh

        ./td -gui

    Click on Download buttion as shown in following image.

.. figure:: https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/get_started/87078310026779781.jpg
  :align: center

  Tang Dynasty SDK in GUI Mode.

#3. Plugin LicheeTang into your computer and hit Refresh buttion on Download Dialog box.

.. figure:: https://fdvad021asfd8q.oss-cn-hangzhou.aliyuncs.com/LicheeTang/get_started/1823555291194601.jpg
  :align: center

.. note:: Due to some unknown bug, JTAG work only with 400kbps or lower speed.

Congratulations, you have setup the TD driver on Linux.
