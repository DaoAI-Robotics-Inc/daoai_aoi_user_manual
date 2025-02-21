2D相机配置（USB端口相机）
=================================

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

7.把AOI中复制的序列号粘贴到sensor_config的json文件中，在Camera_name后面
    .. image:: ./images/19.png
      :scale: 50%
      
