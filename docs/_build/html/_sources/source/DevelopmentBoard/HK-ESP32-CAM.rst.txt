HK-ESP32-CAM
============


硬件简介
********

产品概述
--------

HK-ESP32-CAM模块是弘科设计的一款尺寸为39.8*27*的小型相机模块，此模块可以作为最小系统独立工作。
基于ESP32设计的全新WiFi+蓝牙双模式开发板，采用PCB板载天线，带有2个高性能的32位LX6CPU,采用7级别
流水线架构，主频调整范围80MHz到240Mhz。超低功耗，深度睡眠电流最低达到6mA。

HK-ESP32-CAM可广泛应用于各种物联网场合，适用于家庭智能设备、工业无线控制、无线监控、QR无线识别，
无线定位系统信号以及其它物联网应用，是物联网应用的理想解决方案。

HK-ESP32-CAM采用DIP封装，直接插上底板即可使用，可靠的连接方式，方便应用于各种物联网硬件终端场合。

体积超小的802.11b/g/n Wi-Fi + BT/BLE SoC模块。

产品特性
--------

采用低功耗双核32位CPU，可作应用处理器

主频高达240MHz，运算能力高达 600 DMIPS

内置 520 KB SRAM，外置8MB PSRAM

支持UART/SPI/I2C/PWM/ADC/DAC等接口

支持OV2640和OV7670摄像头，内置闪光灯

支持图片WiFI上传

支持TF卡

支持多种休眠模式

内嵌Lwip和FreeRTOS

支持 STA/AP/STA+AP 工作模式

支持 Smart Config/AirKiss 一键配网

支持二次开发

应用场景
--------

家庭智能设备图传

无线监控

智慧农业

QR无线识别

无线定位系统信号

以及其它物联网应用

技术规格
--------

==================  =================================
参数          		描述
==================  =================================
工作电压			4.75-5.25V
SPIFlash			默认 32Mbit
RAM	内部 			520KB+外部 8MB PSRAM
Wi-Fi				802.11b/g/n/e/i
蓝牙				蓝牙 4.2BR/EDR和 BLE标准
支持接口（2Mbps）	UART、SPI、I2C、PWM
支持 TF卡			最大支持 4G
IO口				9个
串口速率			默认 115200bps
频谱范围			2400 ~2483.5MHz
天线形式			板载 PCB 天线 , 增益 2dBi
图像输出格式		JPEG(仅 OV2640支持),BMP,GRAYSCALE
封装方式			DIP-16

发射功率			
					802.11b:17±2dBm (@11Mbps)
					
					802.11g:14±2dBm (@54Mbps)
					
					
					802.11n:13±2dBm (@MCS7)
					
接收灵敏度			
					CCK,1Mbps:-90dBm

					CCK,11Mbps:-85dBm
					
					6Mbps(1/2BPSK):-88dBm
					
					54Mbps(3/464-QAM):-70dBm
					
					MCS7(65Mbps,72.2Mbps):-67dBm
					
					功耗	关闭闪光灯:180mA@5V
					
					开启闪光灯并且亮度调到最大:310mA@5V
					
					Deep-sleep:最低功耗可以达到 6mA@5V
					
					Moderm-sleep:最低可达到 20mA@5V					
					Light-sleep:最低可达到 6.7mA@5V
安全性				WPA/WPA2/WPA2-Enterprise/WPS
工作温度			-20 ℃~ 70 ℃
存储环境			-40 ℃~ 125 ℃, < 90%RH
重量				10g
==================  =================================

管脚定义
--------

==================  =================================
CAM引脚名称        	ESP32引脚方向
==================  =================================		
D0					PIN5
D1					PIN18
D2					PIN19
D3					PIN21
D4					PIN36
D5					PIN39
D6					PIN34
D7					PIN0
XCLK				PIN22
PCLK				PIN25
VSYNC				PIN23
SDA					PIN26
SCL					PIN27
POWER PIN			PIN32
==================  =================================

==================  =================================
SD引脚名称        	ESP32引脚方向
==================  =================================		
CLK					PIN14
CMD					PIN15
DATA0				PIN2
DATA1/闪光灯		PIN4
DATA2				PIN12
DATA3				PIN13
==================  =================================

.. figure:: ../../_static/HK-ESP32-CAM/CAM.png
    :align: center
    :alt: HK-ESP32-CAM
    :figclass: align-center

    HK-ESP32-CAM
	
	
	
软件示例
********

Arduino IDE平台示例
-------------------

.. important::

	如果您还没有搭建Arduino开发环境，可以参考
	:doc:`../Arduino/ESP32Arduino`

.. important::

	如果您想下载全部示例代码，请点击下方链接来下载。如果您只想下载某一个示例，可以在对应的示例下载

	 `下载HK-ESP32-CAM所有示例`_. （提取码：eeq4）

.. _下载HK-ESP32-CAM所有示例: https://pan.baidu.com/s/1FE0oz8Wa--NKt5GyG7q05Q

ESP32-CAM视频流和拍照示例
^^^^^^^^^^^^^^^^^^^^^^^^^

(1) **点击下方链接下载Camera示例**

	`下载Camera示例`_. （提取码：7cld）

.. _下载Camera示例: https://pan.baidu.com/s/1VSRq1r4uuFC9FuJgUIHqwg


(2) **下载完成后，进入"Camera"目录下，双击打开"Camera.ino"**

.. figure:: ../../_static/HK-ESP32-CAM/CAM-1.png
    :align: center
    :figclass: align-center


(3) **选择开发板，选择端口，上传代码**

.. figure:: ../../_static/HK-ESP32-CAM/CAM-2.png
    :align: center
    :figclass: align-center


(4) **打开串口,选择波特率115200，复位开发板，查看串口输出**

.. figure:: ../../_static/HK-ESP32-CAM/CAM-3.png
    :align: center
    :figclass: align-center

(5) **访问视频流服务器**

	您可以打开手机WIFI，用手机连接上"ESP-xx:xx:xx:xx:xx:xx"（每个开发板的后缀不同）。打开浏览器并键入192.168.4.1地址。按Start Streaming按钮开始视频流。按下Get Still拍照，照片存储在sd卡中，照片名字随机命名
	
.. figure:: ../../_static/HK-ESP32-CAM/CAM-4.png
    :align: center
    :figclass: align-center








	