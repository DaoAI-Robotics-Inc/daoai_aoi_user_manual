AOI&&modbus通信使用
============================


 配置文件步骤
---------------------

1. **获取aoi_comm_config文件和MbslaveAOI**：
   从 `下载中心 <https://daoairoboticsinc-my.sharepoint.com/:f:/g/personal/yangzhipeng_welinkirt_com/EnWE_-lxva1LkYyAklBmnNsBDxP4h7gmuIAlUBEVOlMNSw?e=NcPDJu>`_ 下载文件。

2. **下载aoi_comm_config文件后放置于AOI根目录中**：
    .. image:: ./images/130.png
      :scale: 80%

aoi_comm_config文件参数详解
-----------------------------------------
    .. image:: ./images/131.png
      :scale: 80%

| plc_server_info: 表示PLC的地址和端口号
| capture_coil_address: 0
| 表示为拍照检测(光电感应)信号地址 PLC给AOI
| plc_result_address: 3
| 拍照检测结果地址 AOI给PLC
| red coil address:4
| 检测三色灯为红地址 AOI给PLC
| green_coil_address: 5
| 检测三色灯为绿地址 AOI给PLC
| yellow_coil_address: 6
| 检测三色灯为黄地址 AOI给PLC
| capture_valid_coil_address: 2
| 拍照检测信号是否有效 PLC给AOI
| serial_no_valid_coil_address: 1
| 扫码内容是否有效地址   PLC给AOI
| serial_no_register_address: 0
| 扫码枪内容地址 PLC给AOI 
| capture_finished_coil_address: 7
| 拍照检测完成信号地址 AOI给PLC
| capture_signal_timeout_ms: 3000
| 等待检测信号超时时间
| modbus_poll_interval_ms: 10
| 轮询间隔时间
| enable_serial_no_valid_signal: false
| 是否使用扫码枪 false为关闭 true为打开
| enable_capture_signal: true
| 是否采集PLC信号 true为打开
| enable_switch_product: false
| 是否切换产品 false为关闭
| enable_capture_finished_signal: true
| 采集完成开关，是否发送采集完成信号

AOI的modbus通讯
-------------------------------

1.打开MbslaveAOI软件，点击连接
    .. image:: ./images/132.png
      :scale: 50%

2.打开AOI软件，在检测任务中选择我们的产品
    .. image:: ./images/133.png
      :scale: 50%

3. 在MbslaveAOI中，双击线圈2的地址内容，选择ON，点击OK
    .. image:: ./images/134.png
      :scale: 50%
    
    当产品检测NG，MbslaveAOI中检测结果为0，三色灯信号红色为1

    .. image:: ./images/136.png
      :scale: 50%
    .. image:: ./images/135.png
      :scale: 50%

    当产品检测NG，MbslaveAOI中检测结果为1，三色灯信号绿色为1

    .. image:: ./images/137.png
      :scale: 50%
    .. image:: ./images/138.png
      :scale: 50%

    