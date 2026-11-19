# 出厂固件

[English](README.md)

请按板卡型号选择固件。以下文件均为适用于 16 MB Flash 的 ESP32-S3 合并镜像。

| 型号 | 分辨率 | 触摸 | 固件 | 烧录偏移 |
| --- | --- | --- | --- | --- |
| ESP32-S3-Touch-LCD-5 | 800 × 480 | 有 | [ESP32-S3-Touch-LCD-5_FactoryOnly_20261016.bin](ESP32-S3-Touch-LCD-5_FactoryOnly_20261016.bin) | `0x0` |
| ESP32-S3-Touch-LCD-5B | 1024 × 600 | 有 | [ESP32-S3-Touch-LCD-5B_FactoryOnly_20261016.bin](ESP32-S3-Touch-LCD-5B_FactoryOnly_20261016.bin) | `0x0` |
| ESP32-S3-LCD-5 | 800 × 480 | 无 | [ESP32-S3-LCD-5_FactoryOnly_20260902.bin](ESP32-S3-LCD-5_FactoryOnly_20260902.bin) | `0x0` |
| ESP32-S3-LCD-5B | 1024 × 600 | 无 | [ESP32-S3-LCD-5B_FactoryOnly_20260902.bin](ESP32-S3-LCD-5B_FactoryOnly_20260902.bin) | `0x0` |

使用 esptool 5，在本目录下运行与型号对应的命令，将 COMx 换成实际串口。

~~~sh
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-Touch-LCD-5_FactoryOnly_20261016.bin
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-Touch-LCD-5B_FactoryOnly_20261016.bin
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-LCD-5_FactoryOnly_20260902.bin
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-LCD-5B_FactoryOnly_20260902.bin
~~~
