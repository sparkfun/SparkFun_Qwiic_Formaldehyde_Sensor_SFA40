# Quick Start Guide

In this Quick Start guide we'll wire the SparkFun Formaldehyde Sensor - SFA40 (Qwiic) into a Qwiic circuit with a RedBoard IoT - RP2350 to get formaldehyde readings from the sensor in just a few short minutes. This guide assumes users have a working knowledge of the Qwiic ecosystem, Arduino IDE and using Arduino libraries. If you're not familiar with those topics or want to learn more about the SFA40, we recommend reading through the other sections of the Hookup Guide.

## Basic Assembly

Since this is a Qwiic breakout, all we need to do is connect it to the RedBoard using a Qwiic cable and then plug the RedBoard into a computer over USB:

[Photo showing completed Qwiic circuit with RedBoard IoT - RP2350](/img/Qwiic_Formaldehyde-Action.jpg)

## Arduino Example

* Open the [Arduino IDE](https://www.arduino.cc/en/software/)
* Install the SparkFun SFA40 Arduino library by searching for "SparkFun SFA40" in the [Libraray Manager tool](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-installing-a-library/). Note, this library requires the SparkFun Toolkit to be installed as well. Install that library by searching for "SparkFun Toolkit" in the Library Manager.
* Open "Example01-BasicReadings" from the SFA40 library. Select your Board and Port and click the "Upload" button.
* After the code finishes uploading, open the [serial monitor](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor/) with the baud set to **15200**.
* The SFA40 needs to warm up after power-on. For the first minute the sensor is not ready and the formaldehyde output is forced to 0. Between roughly 1 and 10 minutes the sensor is ready but not yet within specifications. After about 10 minutes the formaldehyde reading is within specifications.