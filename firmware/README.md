# Factory firmware

[简体中文](README_ZH.md)

Select the firmware for your exact model. These are merged images for ESP32-S3 boards with 16 MB Flash.

| Model | Resolution | Touch | Firmware | Flash offset |
| --- | --- | --- | --- | --- |
| ESP32-S3-Touch-LCD-5 | 800 × 480 | Yes | [ESP32-S3-Touch-LCD-5_FactoryOnly_20261016.bin](ESP32-S3-Touch-LCD-5_FactoryOnly_20261016.bin) | `0x0` |
| ESP32-S3-Touch-LCD-5B | 1024 × 600 | Yes | [ESP32-S3-Touch-LCD-5B_FactoryOnly_20261016.bin](ESP32-S3-Touch-LCD-5B_FactoryOnly_20261016.bin) | `0x0` |
| ESP32-S3-LCD-5 | 800 × 480 | No | [ESP32-S3-LCD-5_FactoryOnly_20260902.bin](ESP32-S3-LCD-5_FactoryOnly_20260902.bin) | `0x0` |
| ESP32-S3-LCD-5B | 1024 × 600 | No | [ESP32-S3-LCD-5B_FactoryOnly_20260902.bin](ESP32-S3-LCD-5B_FactoryOnly_20260902.bin) | `0x0` |

With esptool 5, run the command for your model from this directory. Replace COMx with the serial port.

~~~sh
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-Touch-LCD-5_FactoryOnly_20261016.bin
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-Touch-LCD-5B_FactoryOnly_20261016.bin
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-LCD-5_FactoryOnly_20260902.bin
esptool --chip esp32s3 --port COMx write-flash 0x0 ESP32-S3-LCD-5B_FactoryOnly_20260902.bin
~~~
