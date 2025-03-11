
通过局域网访问AOI系统
=================================


1.打开桌面的DaoAI AOI快捷方式
    .. image:: ./images/图片1.png
      :scale: 100%
  
2.点击OK
    .. image:: ./images/110.png
      :scale: 60%
  再次点击红框内的链接

    .. image:: ./images/112.png
      :scale: 60%
  即可进到AOI的系统中
    .. image:: ./images/113.png
      :scale: 60%
      
3.打开命令提示符，输入ipconfig,找到本机电脑的地址，记住此地址
    .. image:: ./images/114.png
      :scale: 60%
   
4.在同局域网下的另一台电脑上，打开浏览默输入我们之前记住的地址, 前端的端口为 80， 默认可以省略，所以直接输入ip即可。
    .. image:: ./images/115.png
      :scale: 60%
  
5.在后端地址栏中 可以输入 同样的地址 再加上 端口号 8000, 如， 192.168.100.183:8000
    .. image:: ./images/backend_addr.png
      :scale: 60%

  进入后即可实现同局域网下的AOI访问
    .. image:: ./images/116.png
      :scale: 60%