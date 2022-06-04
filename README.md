# Arduino ROS Sketchbook

### Description
Arduino sketches for the NVidia Jetbot/Jetracer platforms. Both of the following use rosserial (assumed to be installed) to communicate with ROS over serial. The Jetracer was built first and then the electronics were moved to the Jetbot chassis. So, a lot of the code from Jetracer is migrated to Jetbot.

* jetbot2_nano328o
  * Sketch for the Arduino Nano 328 (old bootloader) on the Jetbot
  * Subscribes to the 'mode' topic of Int8 type
  * Controls Neopixel strip LED colors according to the selected mode
* jetracer2_nano3280
  * Sketch for the Arduino Nano 328 (old bootloader) on the Jetracer
  * Subscribes to the 'mode' topic of Int8 type and controls Neopixel strip LED colors (TODO)
  * Reads the hall effect sensor output via a hardware interrupt and computes speed which is published over rosserial
Code is uploaded using the Arduino IDE on the Jetson Nano with Neopixel and Rosserial libraries installed.

