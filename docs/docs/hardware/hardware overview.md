# Hardware Overview

## SFA40 Formaldehyde Sensor

The SFA40 formaldehyde sensor from Sensirion is a compact electrochemical indoor gas sensor designed to measure concentrations of formaldehyde gas. It has very low cross-sensitivity with similar, common indoor gases like ethanol and nitrogen dioxide. It's intended to measure indoor gas concentrations over long periods of time and has a long-term drift of <5ppb (or <5% of the measured value, whichever is larger) per year. The sensor includes humidity and temperature sensing to compensate the formaldehyde signal. Each SFA40 has a unique 48-bit serial number and self-test for verifying the sensor's electrical connections.

The SFA40 provides a calibrated digital output with an accuracy of &plusmn;20ppb (parts per billion) or &plusmn;20% of the total measurement range of 0 to 2000ppb. The sensor does require a 10 minute calibration period on power up. The SFA40 accepts a supply voltage 1.6 to 3.6V (3.3V over Qwiic) and draws an average of 80&micro;A during measurement with a max of 6mA. While idle it draws an average of 60&micro;A.

## Connectors

### Qwiic Connectors

The board has a pair of Qwiic connectors to make it easy to integrate into a Qwiic circuit. These connect to the SFA40's I<sup>2</sup>C signals along with 3.3V and ground to power the board and communicate with the SFA40.

### Plated Through-Hole (PTH) Header

The board also routes the same signals as the Qwiic connectors (SDA, SCL, 3.3V and Ground) to a 0.1"-spaced plated through-hole header for users who prefer a soldered connection.

## LED

The lone LED on this breakout is a red power status LED.

## Solder Jumpers

The board has two solder jumpers labeled **LED** and **I<sup>2</sup>C**. The **LED** jumper completes the power LED circuit and is CLOSED by default. Open this jumper to disable the power LED. The **I<sup>2</sup>C** jumper is a three-way jumper that pulls the SFA40's SDA and SCL lines to **3.3V** through a pair of **2.2k**&ohm; resistors and is CLOSED by default. Completely open this jumper to disable pullups on the I<sup>2</sup>C bus if necessary.

## Board Dimensions

This breakout matches the Qwiic standard and measures 1" x 1" (22.5mm x 22.5mm) and has four mounting holes that fit a 4-40 screw.