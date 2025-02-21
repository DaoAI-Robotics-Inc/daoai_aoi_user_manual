DAOAI AOI 用户指南
==============================

产品定位
---------------

DaoAI AOI（Automated Optical Inspection） 是一款面向工业精密制造领域的智能表面缺陷检测系统，
专为高精度、高效率的缺陷检测需求设计。系统深度融合机器视觉、深度学习算法与自动化控制技术，
旨在为汽车零部件、半导体、精密模具、电子元器件等行业的客户提供全自动、高可靠性的表面缺陷检测解决方案，
帮助用户提升产品质量、降低人工成本，并实现生产过程的数字化与智能化升级。

核心功能
--------------

一键建模，快速缺陷检测
~~~~~~~~~~~~~~~~~~~~~~~~~~

- **单张无缺陷样本建模**：仅需 **1 张无缺陷图片** 作为参考，即可 **自动生成检测模型**，无需大量缺陷样本。
- **支持多区域检测**：用户可在 **同一物体上设定多个检测区域**，AI 独立分析每个区域的缺陷，提高检测精度和灵活性。

高效 AI 训练与推理
-------------------
- **超快速训练**：模型训练仅需 **约 1 分钟**，即可投入生产使用。
- **极速推理**：检测速度 **仅 10ms/组件**，满足 **高速产线** 的实时检测需求。
- **持续优化**：检测过程中，如发现 **推理错误**，可 **人工反馈** 并重新训练模型，使检测更精准。

先进的 3D & 2D 视觉检测
~~~~~~~~~~~~~~~~~~~~~~~~~~

- **DaoAI 3D 相机**：采用 **结构光成像**，可 **精准检测 0.1mm 级别缺陷**，支持 **物体高度测量、安装偏差分析** 等高级功能。
- **USB 2D 工业相机支持**：兼容 **USB 接口的高分辨率 2D 工业相机**，适用于 **表面缺陷检测**，可灵活适配不同产线需求。

智能检测历史 & AI 反馈
~~~~~~~~~~~~~~~~~~~~~~~~~~

- **检测记录存储**：每次检测结果 **完整存档**，支持查询 **缺陷数量、位置、缺陷率等详细信息**。
- **AI 误判反馈**：可 **实时反馈 AI 误判** 或 **历史记录回溯反馈**，实现 **智能自学习优化**，不断提升检测精度。

工业级数据通讯与集成
~~~~~~~~~~~~~~~~~~~~~~~~~~

- **Modbus 通讯**：支持 **Modbus 协议**，可与 **产线设备无缝对接**，实现自动化协同工作。
- **兼容工业系统**：可与 **MES、ERP、PLC** 等系统集成，实现 **检测数据实时上传、生产指令交互**。


.. toctree::
   :maxdepth: 2
   :caption: 快速入门

   quick_start/index

.. toctree::
   :maxdepth: 2
   :caption: 操作全流程指南

   application/start_program
   application/international/index
   application/2D_camera
   application/camera_config
   application/infield_cali
   application/new_project
   application/ROI
   application/detect_mode
   application/NG
   application/data_export

.. toctree::
   :maxdepth: 2
   :caption: 应用案例库

   case_study/index

.. toctree::
   :maxdepth: 1
   :caption: 常见问题快速查询表

   support/faq/index
   support/Appendix/index.rst



