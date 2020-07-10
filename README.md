# FPD-LinkIII_Raspberry_HW
FPD-Link III Hardware compatible with Raspberry Pi Camera and Raspberry Pi CSI connector.


```ditaa
/------------------\        /--------------------\        /----------------------\        /-------------------\
| MIPI CSI CAMERA  |        | FPDLINK SERIALIZER |        | FPDLINK DESERIALIZER |        | MIPI CSI RECEIVER |
+------------------+  CSI   +--------------------+        +----------------------+  CSI   +-------------------+
|                  | -----> |                    |  Coax  |                      | -----> |                   |
| Raspberry Pi     |  GPIO  | piCam2fpdlink      | <----> | fpdlink2raspi        |  GPIO  | Raspberry Pi (4)  |
| Camera Module v2 | <----> | PCB                |        | PCB                  | <----> | Jetson Nano       |
|                  |   I2C  |                    |        |                      |   I2C  | ...               |
|                  | <----> |                    |        |                      | <----> |                   |
\------------------/        \--------------------/        \----------------------/        \-------------------/
```
