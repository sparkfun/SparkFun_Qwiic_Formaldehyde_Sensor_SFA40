# Troubleshooting

## Stabilization Period

The SFA40 requires a stabilization of approximately 10 minutes before it returns formaldehyde readings that are within the sensor's specifications. During the first minute after power-up or reset it returns formaldehyde readings of 0. After the first minute, the sensor returns formaldehyde readings but they are not considered within specification by the sensor. The SFA40 reports a status indicator byte to allow users to determine what state the sensor is in. Example 4 in the SparkFun SFA40 Arduino Library demonstrates how to poll the SFA40 for the status byte to determine the validity of formaldehyde data.

## Support

If you need technical assistance or more information on a product that is not working as you expected, we recommend heading on over to the [SparkFun Technical Assistance](https://www.sparkfun.com/technical_assistance) page for some initial troubleshooting.

If you need technical assistance and more information on a product that is not working as you expected, visit the [SparkFun Community](https://community.sparkfun.com). The community forums are monitored by the SparkFun Technical Support Team and the SparkFun community as a whole. If this is your first visit to our forum, you'll need to create a [Forum Account](https://forum.sparkfun.com/ucp.php?mode=register) to post questions.

        