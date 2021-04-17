
Eclipse IDE开发环境设置(插件版)
*******************************

先决条件
运行IDF Eclipse插件的最低要求是：

.. important::

	Java 11及更高版本：点击下载并安装 `Java SE`_.
	
	Python 3.5及更高版本：点击下载并安装 `Python`_.
	
	Git：获取最新的git: 点击下载并安装  `Git`_.
	
	ESP-IDF 4.0及更高版本：克隆ESP-IDF存储库


.. _Java SE: https://www.oracle.com/java/technologies/javase-downloads.html

.. _Python: https://www.python.org/downloads/

.. _Git: https://git-scm.com/downloads


（1） **下载C/C++版的eclipse**

	点击下载 `eclipse`_. 

.. _eclipse: https://www.eclipse.org/downloads/packages/

.. figure:: ../../_static/Eclipse-Plugin/1.png
    :align: center
    :figclass: align-center


（2） **安装IDF插件，打开eclipse，，Espressif IDF从列表中选择并继续安装**

.. figure:: ../../_static/Eclipse-Plugin/2.png
    :align: center
    :alt: 点击Help->Install New Software
    :figclass: align-center

    点击Help->Install New Software



	

.. figure:: ../../_static/Eclipse-Plugin/3.png
    :align: center
    :alt: 
    :figclass: align-center

    点击Add…，输入Name为Espressif IDF Plugin for Eclipse，输入Location存储库https://dl.espressif.com/dl/idf-eclipse-plugin/updates/latest/
	
.. figure:: ../../_static/Eclipse-Plugin/4.png
    :align: center
    :alt: 
    :figclass: align-center

    勾选Espressif IDF，点击Next

.. figure:: ../../_static/Eclipse-Plugin/5.png
    :align: center
    :alt: 
    :figclass: align-center

    点击Next，
	
.. figure:: ../../_static/Eclipse-Plugin/6.png
    :align: center
    :alt: 
    :figclass: align-center

    勾选l accept the terms of the license agreements，点击Finish

.. figure:: ../../_static/Eclipse-Plugin/7.png
    :align: center
    :alt: 
    :figclass: align-center

    确认安装

.. figure:: ../../_static/Eclipse-Plugin/8.png
    :align: center
    :alt: 
    :figclass: align-center

    接受证书
	
.. figure:: ../../_static/Eclipse-Plugin/9.png
    :align: center
    :alt: 
    :figclass: align-center

    重启IDE
	

（3） **安装ESP-IDF工具**

.. figure:: ../../_static/Eclipse-Plugin/10.png
    :align: center
    :alt: 
    :figclass: align-center

    选择Help> ESP-IDF Tools Manager>Install Tools
	
.. figure:: ../../_static/Eclipse-Plugin/11.png
    :align: center
    :alt: 
    :figclass: align-center

    提供ESP-IDF Directory路径，提供Git和Python可执行位置（如果未自动检测）。单击Install Tools以继续安装过程。检查控制台以获取安装详细信息。如果您是第一次安装，则可能需要一段时间，因为它必须下载并安装xtensa-esp32-elf，esp32ulp-elf，cmake，openocd-esp32和ninja工具。

（4） **创建一个新项目**

.. figure:: ../../_static/Eclipse-Plugin/12.png
    :align: center
    :alt: 
    :figclass: align-center

    点击Window-> Perspective-> Reset Perspective..

.. figure:: ../../_static/Eclipse-Plugin/13.png
    :align: center
    :alt: 
    :figclass: align-center

    转到File> New> Espressif IDF Project

.. figure:: ../../_static/Eclipse-Plugin/14.png
    :align: center
    :alt: 
    :figclass: align-center

    转到File> New> Espressif IDF Project，提供 Project name（这里以hello_world为例），点击Next

.. figure:: ../../_static/Eclipse-Plugin/15.png
    :align: center
    :alt: 
    :figclass: align-center

    转到File> New> Espressif IDF Project，选择hello_world



（6） **配置启动目标**

.. figure:: ../../_static/Eclipse-Plugin/16.png
    :align: center
    :alt: 
    :figclass: align-center

    先将ESP设备已连接到您的电脑，点击第三个下拉菜单，选择 New Launch Target

.. figure:: ../../_static/Eclipse-Plugin/17.png
    :align: center
    :alt: 
    :figclass: align-center

    选择ESP Target，点击Next
	
.. figure:: ../../_static/Eclipse-Plugin/18.png
    :align: center
    :alt: 
    :figclass: align-center

    这里Name为目标输入hello_word（可以自定义名字） ** ，IDF Target 是esp32， Serial Port我这里是COM18（一般会自动识别） **


（7） **编译项目**

.. figure:: ../../_static/Eclipse-Plugin/19.png
    :align: center
    :alt: 
    :figclass: align-center

    单击在Build工具栏最左侧看到的按钮小部件，编译完成如图中的②

（8） **烧录项目**


.. figure:: ../../_static/Eclipse-Plugin/20.png
    :align: center
    :alt: 
    :figclass: align-center

    单击启动按钮（左侧的第二个按钮）即可启动Flash操作

（9） **查看串行输出**

.. figure:: ../../_static/Eclipse-Plugin/21.png
    :align: center
    :alt: 
    :figclass: align-center

    单击Open a Terminal工具栏上的图标

.. figure:: ../../_static/Eclipse-Plugin/22.png
    :align: center
    :alt: 
    :figclass: align-center

    配置ESP-IDF Serial Monitor来连接到串行端口，默认情况下，波特率和串行端口设置是自动配置的。


.. figure:: ../../_static/Eclipse-Plugin/23.png
    :align: center
    :alt: 
    :figclass: align-center

    查看串行输出

至此，我们已经完成了hello_word项目的烧录，可以尝试其他项目的烧录
以上介绍的是创建新项目，您也可以导入本地现有项目
在File->import...，在Espressif菜单列表中选择Existing IDF Project，点击Next，单击Browse...以选择一个现有的项目位置目录，提供Project name，点击Finish。

（10） **配置项目**

	在终端我们需要输入idf.py menuconfig 来打开配置项目，而IDF插件可以使您sdkconfig无需离开Eclipse环境即可进行配置

.. figure:: ../../_static/Eclipse-Plugin/24.png
    :align: center
    :alt: 
    :figclass: align-center

    导航到sdkconfig文件，双击该文件以启动SDK配置编辑器，这里就类似我们终端的配置项目，可以根据需要配置项目

（11） **ESP-IDF应用程序大小分析**

	右键点击项目，选择ESP-IDF: Application Size Analysis菜单选项以启动编辑器

（12） **ESP-IDF终端** 

	单击Open a Terminal工具栏上的图标，ESP-IDF Terminal从终端下拉菜单中选择，然后单击OK以启动终端

（13） ** **升级现有的IDF Eclipse插件**

	点击Help-> Check for Updates，如果找到更新，请选择Espressif IDF Plugins for Eclipse并取消选择所有其他项目，单击Next以继续安装