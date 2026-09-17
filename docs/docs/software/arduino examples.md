# Arduino Examples

## Example 01 - Basic Readings

The first example demonstrates how to set up the SFA40 and get basic readings from the sensor for formaldehyde (HCHO), relative humidity and temperature. Reminder, the SFA40 requires a 10 minute stabilization period after power up so for the first minute the formaldehyde readings will report as "0". After the first minute, it will output HCHO in ppb but these values are not within the sensor's specification until the sensor has been running for 10 minutes. Example 04 - Status shows how to read the status reports from the SFA40 to get a better idea of when the sensor is ready to report stabilized formaldehyde concentrations.

## Example 02 - Serial Number

The second example shows how to poll the SFA40 for its serial number. Each SFA40 comes with an individual 48-bit serial number that is both etched onto the physical sensor and available for polling using software. This sketch reads it and prints it as a 12-digit hexadecimal value, which matches the serial number laser-marked on the metal cap of the sensor.

## Example 03 - Self Test

The third example demonstrates how to perform a self test on the SFA40 to verify electrical connections and functionality of the sensor. This is mostly used during production but can help diagnose issues with the SFA40 to determine if there is a hardware fault.

## Example 04 - Status

The fourth example shows how to interpret the status variable the SFA40 returns with every measurement. The SFA40 requires about 10 minutes after power up to return valid measurements.

The example simulates a full power-on state by performing a soft reset. For the first minute after this reset, the sensor is "not ready" and reports only 0 formaldehyde concentration. Between one minute and ten minutes, the SFA40 is ready but "not yet within specifications". After ten minutes, the sensor is now within specifications and reports stabilized formaldehyde readings. The main loop then reads the status report from the SFA40 and prints out "Sensor warming up (not ready)" during the first minute, then prints out "Stabilizing (HCHO ~) ppb, not yet within spec" for the stabilization period. After this finishes, it prints out stabilized readings.
