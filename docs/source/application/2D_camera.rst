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


虚拟相机
------------------------

配置虚拟相机需要替换安装目录下的 ``capture agent\`` 文件夹中的 ``capture_agent.dll`` 文件。您可以从下面的链接下载所需的文件：

- `capture_agent.dll.file <https://daoairoboticsinc-my.sharepoint.com/:u:/g/personal/nrd_daoai_com/ESrH67MyqbVGq1e2IEmFNA0BH_R69YFlzA_CcMXWlWkYlA?e=w6IkFf>`_

**步骤如下：**

1. **替换 DLL 文件**

   - 先将当前的 DLL 文件重命名，后缀加上 ``.real``，以避免新文件复制后混淆。
   - 然后，将下载的 ``capture_agent.dll.file`` 复制到 ``capture agent\`` 文件夹下。
   - 最后删除复制后文件名称中的 ``.file`` 后缀，使名称变为 ``capture_agent.dll``。

   .. image:: ./images/file_camera_0.png
      :scale: 60%
      :alt: capture_agent.dll 文件示例

   .. image:: ./images/file_camera_2.png
      :scale: 60%
      :alt: 替换后文件名称示例

|

2. **编辑配置文件**

   - 参考下图，编辑 ``capture_agent_config.json`` 文件，在其中加入如下配置：
     
     ``path: "<图片路径>",``
     
   .. image:: ./images/file_camera_1.png
      :scale: 60%
      :alt: 编辑配置文件示例

|

3. **启动虚拟相机**

   - 重新启动 AOI 软件后，系统将使用虚拟相机，并从配置的路径中读取图片。

   .. image:: ./images/file_camera_3.png
      :scale: 50%
      :alt: AOI 软件读取虚拟相机图片示例

**图片读取规则** :

- 图片文件命名必须为数字加 ``.png`` 后缀，如 ``0.png``。
- 程序会从 ``0.png`` 开始读取，每次拍照时会自动读取下一个数字命名的图片（如 ``1.png``、``2.png``……），形成一条数据链。
- 当从 ``0.png`` 开始读取时，如果找不到 ``1.png``（数据链断开），则程序会循环回到 ``0.png``。
- 例如：如果您希望循环读取一张图（如在定义产品时），可以将文件夹中除 ``0.png`` 外的其它图片（例如 ``1.png``）重命名为其他名称。此时程序从 ``0.png`` 开始读取，由于找不到 ``1.png``，数据链即中断并循环回 ``0.png``。定义完产品后，再将 ``1.png`` 恢复，程序便可读取完整的数据链。

这样设置后，您就能方便地利用虚拟相机功能进行图像采集和产品定义。


