1. Performance wise around Pi Zero 2W range. eMMC 16GB have good speed.
2. There is no SPI/I2C expose via the Pi CM4 connector/40 pin connector
3. Serial is on Pi_RX/TX and working.
4. The actual GPIO list layout as per below. Not all pin work.
5. My board is CB1_eMMC_V1.1, IO voltage is 3.3V, 2x512MB DDR3 RAM, 16GB eMMC.
6. There won’t be RTC support due to no i2C expose.
7. There is no 2nd HDMI, no DSI, no CSI.
8. Extra 3 USB line is using CSI0/1 dataline.
9. Idle at 50’C, full load will go above 70’C. Suggest to put a small heatsink. (40x40mm Stepper motor heatsink)
