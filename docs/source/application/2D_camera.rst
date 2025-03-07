相机连接配置
=================================

2D USB端口相机
--------------------------

1.首先下载并打开Zadig工具
    .. image:: ./images/13.png
      :width: 200px

2.选择Options,点击选中List All Devices
    .. image:: ./images/14.png
      :scale: 50%

3.在列表中选择连接的相机，改为驱动版本为16385（默认就为此版本），点击Reinstall Driver
    .. image:: ./images/15.png
      :scale: 50%

4.打开AOI的界面，点击右下角的设置，选择编辑系统配置
    .. image:: ./images/16.png
      :scale: 50%

5.可以看到提示相机的序列号，复制这个序列号
    .. image:: ./images/17.png
      :scale: 50%

6.从路径中C:\Program Files\DaoAI AOI\capture_agent找到sensor_config的json文件，双击打开，可用记事本的方式进行打开
    .. image:: ./images/18.png
      :scale: 50%

7.把AOI中复制的序列号粘贴到sensor_config的json文件中，在Camera_name后面，并确保 is_3D 是 false
    .. image:: ./images/19.png
      :scale: 50%

8.关闭软件，然后重启进入AOI系统即可自动连接到相机。
      
2D Gige网口相机配置
---------------------------

1.首先应确保正确安装了相机驱动，包含GigE驱动。并且可以用相机官方软件发现。
    .. image:: ./images/hik_install.png
      :scale: 90%

2.打开AOI的界面，点击右下角的设置，选择编辑系统配置
    .. image:: ./images/16.png
      :scale: 50%

3.在发现的相机旁，点击刷新，就可以看到2D相机的序列号，复制这个序列号
    .. image:: ./images/17.png
      :scale: 50%

4.从路径中C:\Program Files\DaoAI AOI\capture_agent找到sensor_config的json文件，双击打开，可用记事本的方式进行打开
    .. image:: ./images/18.png
      :scale: 50%

5.把AOI中复制的序列号粘贴到sensor_config的json文件中，在Camera_name后面，并确保 is_3D 是 false
    .. image:: ./images/19.png
      :scale: 50%

6.关闭软件，然后重启进入AOI系统即可自动连接到相机。

3D AOI相机
------------------------

在配置3D相机只需把is_3D更改为true即可，名字无需更改，3D相机不看这个的名字。
   .. image:: ./images/139.png
      :scale: 50%

.. note::
  请确保相机的 Certificate.bin 文件正确放置在了AOI软件根目录下。