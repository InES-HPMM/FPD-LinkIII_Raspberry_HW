# FPD-LinkIII_Raspberry_HW

FPD-Link III Hardware compatible with Raspberry Pi Camera and Raspberry Pi CSI connector.

[![logo](images/ines_logo.png)](https://www.zhaw.ch/en/engineering/institutes-centres/ines/ "Homepage")

__The group High Performance Multimedia from the Institute of Embedded Systems associated with ZHAW School of Engineering proudly presents a TI FPD-Link III hardware compatible with the Raspberry Pi camera and the Raspberry Pi FFC (FPC, ZIF) camera connector.__

__Additionally we provide an open source driver for TI devices DS90UB954 paired with DS90UB953:__
<https://github.com/InES-HPMM/FPD-LinkIII_ds90ub95x>

> For recent news check out our [Blog](https://blog.zhaw.ch/high-performance/).

## Working Setup

### Overview

![Overview](https://github.com/InES-HPMM/FPD-LinkIII_Raspberry_HW/blob/master/images/overview.png)

```ditaa
/-------------------\        /----------------------\        /--------------------\        /------------------\
| MIPI CSI RECEIVER |        | FPDLINK DESERIALIZER |        | FPDLINK SERIALIZER |        | MIPI CSI CAMERA  |
+-------------------+  CSI   +----------------------+        +--------------------+  CSI   +------------------+
|                   | <----- |                      |  Coax  |                    | <----- |                  |
| Raspberry Pi (4)  |  GPIO  | fpdlink2raspi        | <----> | piCam2fpdlink      |  GPIO  | Raspberry Pi     |
| Jetson Nano       | <----> | PCB                  |        | PCB                | <----> | Camera Module v2 |
| ...               |   I2C  | DS90UB954            |        | DS90UB953          |   I2C  |                  |
|                   | <----> |                      |        |                    | <----> |                  |
\-------------------/        \----------------------/        \--------------------/        \------------------/
```
 
### fpdlink2raspi PCB

![fpdlink2raspi PCB](https://github.com/InES-HPMM/FPD-LinkIII_Raspberry_HW/blob/master/images/fpdlink2raspi.jpg)
 
### piCam2fpdlink PCB

![piCam2fpdlink PCB](https://github.com/InES-HPMM/FPD-LinkIII_Raspberry_HW/blob/master/images/picam2fpdlink.jpg)
 
### Raspberry Pi 4 with MIPI CSI connector

![RaspberryPi 4](https://github.com/InES-HPMM/FPD-LinkIII_Raspberry_HW/blob/master/images/raspi.jpg)
