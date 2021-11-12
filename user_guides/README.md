# SNOdar Quick Start Guide: [PDF](snodar_quick_start_guide.pdf)

[Back](../)

[Quick Start Video Guides](video_guides.md)

## Power and Boot Sensor

1. Unbox and attach the 6-pin power cable to the main connector. The connection is directionally keyed. Make sure to engage the bayonet locking mechanism. 

![](images/snodar_power.png)

2. Supply 6-24 VDC (3.5W supply minimum is needed to test the heater) to the cable leads according to the pinout below (either GND can be used):

| SNOdar Pin Name | SNOdar Pin NO. | Cable Pin NO. |  Wire Color |
| --------------- | -------------- | ------------- | ----------- |
| GND             | 1              | 1             | BLACK       |
| PWR +12V        | 2              | 2             | WHITE       |
| GND             | 3              | 3             | GREEN       |
| SDI-12          | 4              | 4             | RED         |
| TX: RS-232      | 5              | 5             | BLUE        |
| RX: RS-232      | 6              | 6             | VIOLET      |

3. Once powered, look for flashing Green LEDs (20 flashes @ 5 Hz) to indicate _Good Health_ and Bluetooth Low Energy (BLE) advertising. If the LEDs flash RED instead, click on the `Sensor Health` on the _Home_ card to note exactly what failed. THis will aid in support diagnostics. 
4. If in the field go to [Installation and Mounting](#installation-and-mounting) directly below; otherwise, set sensor aside and set up the [SNOdar Mobile App](#download-the-app) on your mobile device.

## Installation and Mounting

### Mounting Height
Mount the sensor less than **9 meters** and more than **9 cm** from the ground or Stormboard fixture.

![](images/snodar_mounting_diagram.png)

As a reference, this is the approximate cone projection field-of-view (FOV) of the SNOdar, when impinging upon the ground or snow surface.

![](images/snodar_fov.png)

### Obliqueness
For best performance, rotationally mount the sensor so that it is normal to the ground, i.e. measuring perpendicular to the ground surface; however, it does have the ability to be mounted at angles or on hillsides, up to 30 degrees from normal.

#### IMU Directionality
- **Roll**: Rotation about the axis running through the clamp mount (this is the rotation monitored in **Stormboard** mode, 20 degrees is ideal)
- **Pitch**: Rotation about the axis running through the connector
- **Yaw**: Rotation about the axis running through the top dome peak

Roll                         |  Pitch                         | Yaw
:---------------------------:|:------------------------------:|:----------------------------:
![](images/snodar_roll.jpg)  |  ![](images/snodar_pitch.jpg)  | ![](images/snodar_yaw.jpg)

### Ground Preparation
Before **Setup** and **Calibration**, clear the ground of any debris, e.g. sticks, rocks, or uneven ground clumps below the sensor. Also, remove and clear large foliage and tall, dense grass below and around the sensor within the cone of influence (based on the mounting height). Ideally, a level dirt/rock pad is prepared below the sensor for the most accurate seasonal measurements. 
- Note: if a dark/black surface, e.g. snow pillow canvas, is the original target, **Calibration** will NOT succeed. This is NOT a valid target.

## Download the App
Depending on your mobile device of choice:

Play Store App                                                                                  |  iOS App Store
:----------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:
[![](../assets/images/google-play-badge.png)](https://play.google.com/store/apps/details?id=com.snodar)   | [![](../assets/images/apple-app-store-badge.png)](https://apps.apple.com/us/app/snodar/id1584974884)

## Run the App

### Permissions
To run the fully featured App, Bluetooth and Location services (i.e. GPS) *MUST* be enabled.

### Connect
![](images/connect_screen.png)
1. To connect to a sensor, tap the **+** sign in the lower right corner of the screen.

2. From the **Add Sensor** screen, connect to the desired sensor by tapping on the **Connect** button by the sensor’s name.

3. When prompted, enter the default passkey `123456` and tap the pair button. 
	- For more information on changing an already connected sensor’s passkey see Security -> Change Passkey.
	
4. Devices that have already been added will be listed on the home screen and can be connected to by tapping the **Bluetooth** button to the right of the device's name.

![](images/connect_button.png)

### Pairing and Bonding Security
The mobile device will now have to pair and bond to the SNOdar device. This is an encryption-based security feature to protect the device and its data from nefarious and/or unintentional actions. Therefore, it is highly important to _Change_ the default passkey and note, somewhere safe, where it can be recalled if forgotten.

### Change Passkey
1. From the home screen, tap on the **Kebab Menu**  beside the name of the desired sensor.
2. Select **Security** from the menu items.
3. Tap the edit button and change the default passkey to a six digit, numeric passkey of your choice.
3. Tap the **Save** button to update the passkey.
	- NOTE: updating the passkey will restart the device

![](images/security_menu.png)

## Sensor Setup
Upon SNOdar sensor field installation, it is imperative to run the **Sensor Setup** located in the **Kebab Menu** on the home screen.

![](images/setup_menu.png)

### Sensor Mode
The Sensor Mode Page allows for different sensor operation modes to be selected.

- The **Snow Depth** sensor mode is standard automated snow depth measurement. The unit needs to be calibrated at the beginning of each season (preferably when NO snow is present) for accurate, settled snow depth measurements.
- The **Stormboard** sensor mode is a manual calibration mode for storm snowfall measurements. This mode will calibrate to 'zero' accumulation after the user wipes the stormboard clean of snow. A manual calibrate after each clear will help the accuracy remain high.
- The **Distance** sensor mode is used for basic distance measurements. This will be the default mode when NO Bluetooth setup can be done. The sensor will measure distance to the snow every 5 minutes and send data out the SDI-12.
- The **Manual** sensor mode has no automated operation only user interactions. This mode is used exclusively for testing and in lab scenarios.

### Mounting: Orientation
The Mounting Orientation page verifies that the sensor is mounted in the proper orientation - less than 10 meters above ground and with the sensor bottom facing towards the ground.

Once the sensor has been mounted press the **Calibrate** button in the bottom middle of the screen. If the sensor is properly oriented, this **Calibrate** button will turn green.

### Mounting: Snow Presence
The Snow Presence Page records if snow is present when sensor is set up. If snow is present, the depth of the snow in meters must be entered.

![](images/setup_one.png)


### Mounting: Distance Calibration
The Sensor Calibration Page allows the sensor to calibrate. To do so clear any obstruction from below the sensor, press the **Calibrate**  button, and stand at least 10 meters away from the sensor.

### Location
The Location Page uses your mobile device's GPS to determine the sensor's location. To update the location tap the **Refresh Coords** button.

### Synchronize
The Synchronize Page synchronizes the sensor's time with the time and time zone of your mobile device. To do so, press the **Synchronize** button. 

When the time has been synchronized, the newly set time will be displayed.

![](images/setup_two.png)

### Name Sensor
The Name Sensor Page allows for the sensor to be given a unique name.

The name can be reverted back to the original sensor name by pressing the **Refresh** icon to the right of the text input field.

### Snowfall
The Snowfall page allows for a time to be set at which the snowfall calculations for the day and the season will start over. To set the seasonal reset date, tap the date icon under the **Resets @** button and scroll through the year, month, and date. To set the daily reset time, scroll through the time options under the **Resets @** button. Both values are set according to the local time of the mobile device. 

### Snow Class
The Snow Class Page allows for the type of snow to be specified. Choose a snow class that best describes the snow in your region.
- Alpine
- Maritime
- Prairie
- Tundra
- Taiga

![](images/setup_three.png)

### Measurement Interval
The Measurement Interval Page allows for the interval at which measurements are taken to be set. The minimum allowable time interval is 1 minute.

To set the interval, tap anywhere on the current hours and minutes listing. Then tap the time button that appears. To increase the time, drag the hours (left) or minutes (right) up. To decrease the time, drag the hours (left) or minutes (right) down. Tap anywhere outside of the time input to exit.

### External Logging
The external logging configuration for off-board data acquisition devices controls RS-232 and SDI-12 commications and settings. RS-232 can be disabled, set to transmit measurement data as an ASCII formatted string to any device listening on the RS-232 port, or can be set to communicate with an Irdium Short Burst Data (SBD) Satcom. The SDI-12 port, commonly used to communicate with data loggers, is always on and listening. It can be configured to output measurement data in two different formats:
- Metric: distances in Meters and Temperatures in degrees Celsius.
- SNOTEL: distances in Inches and Temperatures in degrees Celsius.

### Enhanced Temperature Control
While the SNOdar has a standard temperature control, the Enhance Temperature Control page allows for the temperature control to be disabled or set to Line Powered control. Detailed information about each of these options can be found by tapping the more info button. 

![](images/setup_four.png)

### Complete Setup
Lastly, the Complete Setup Page provides a summary of the settings. Any setup steps that were skipped or are incomplete will have a red **x** next to them. To go back to these steps, press the menu button in the right corner of the setup page and choose the desired setup step from the menu.  

To confirm the settings and complete the sensor setup, press the **Save Settings** button.

![](images/setup_menu_button.png)

### Erase Data Flash
Once you press the **Save Settings** button, you will be asked if you would like to format the device storage. By choosing yes the device storage will be formatted ***and any recorded data will be deleted***. By choosing no, the device storage will not be formatted and any recorded data will be preserved. 

![](images/setup_formatStorage.png)

## View
To view a sensor and its associated data, press the **View** button on the desired sensor’s tab. You can return to the home page via the back arrow in the top left corner. 

![](images/view_button.png)

![](images/view_toolbar.png)

### Summary 
The Summary Page provides an overview of the sensor's data as well as displays any errors with the sensor. For more information on sensor error notifications see the ***Sensor Error Notifications*** section of the user guide.
The Summary Page contains information on snow depth, sensor storage, measurement information, sensor power, internal sensor temperature including potential heater failure, and sensor orientation including potential sensor drift.  

![](images/view_summary.png)

### Logs
The Logs Page displays data that has been downloaded for the sensor. To download data, press the **Download** button in the lower right hand corner of the page. Then press the **Download Log from Sensor** button. You will be prompted to choose data from either the last day, the last week, or the last month. A custom range can also be selected by tapping on the first displayed date or time and setting a unique time then doing the same for the second displayed date or time. Once downloaded, the logs page will display all logs that have been downloaded to your mobile device.  

![](images/log_download.png)

More information about each log can be found under the **SNOLOG Information** button. To view a graph of the log, tap the **View** button. Tapping the **Share** button will bring up options for sharing the log or uploading to your cloud storage of choice. 

![](images/view_share_button.png)

### Data
The Data Page displays an interactive depiction of the downloaded data. To plot data, select a log and press the **View** button for that log. Once the log has been plotted, different collections of data can be displayed by tapping the **Dropdown menu** above the plot.  The chart settings can also be altered by tapping the **Settings** icon beside the dropdown menu. 

![](images/view_data.png)

### Config
The Config Page allows for quick edits of some of the sensor's settings. These settings can only be edited after the **Unlock** button in the bottom corner of the screen is tapped. The **Lock** button should be tapped after edits are made. 

![](images/view_config.png)

## Appendix

### Device Firmware Update (DFU)

The App has the ability to update the sensor firmware over-the-air (OTA). Toggle the main _Kebab_ menu in the upper left corner of the sensor card on the _Home_ page. If there is an available update, a red-encircled `+` alert will appear by the _Update_ action. Initiate the update and the unit LEDs will quickly flash Magenta, then hold Cyan while it is updating. DON'T power down the sensor or quit the App while updating. The unit will reboot and flash Green when updated and ready.

Sensor Card Kebab Menu Location         |  Available Firmware Update
:--------------------------------------:|:------------------------------------------------:
![](images/dfu_menu.png)            | ![](images/dfu_update.png)

### LED Legend

- Upon Boot
	- 4 secs @ 5 Hz Green: Health Diagnostics **Passing**
	- 4 secs @ 5 Hz Red: Health Diagnostics **Failure**
- Measurement
	- Solid Yellow for length of measurement
	- Solid White for length of calibration
- BLE Connect
	- Fade Blue -> Cyan -> White for 2 seconds
- BLE Disconnect
	- Fade White -> Cyan -> Blue for 2 seconds
- Device Firmware Update (DFU) via Mobile device
	- Magenta for 2 seconds preparing update into Cyan for the length of the upload, up to 60 seconds. The unit will reboot when updating is finished.
- `Find Me` Feature on the _Home_ Kebab menu
	 - Blue <-> White ping-pong for 4 seconds
	 - Useful to identify units when there are multiple sensors to configure

### Sensor Error Notifications

- Orientation Drift (on the left): This sensor orientation notification will appear if considerable drift has been detected in the sensor's orientation. This error can be resolved by adjusting the sensor back to the correct orientation.
- Heater Failure (on the right): This notification will be seen if the sensor's internal heater fails.

Orientation Drift Notification                      |  Heater Failure Notification
:--------------------------------------------------:|:------------------------------------------------:
![](images/sensor_orientation_notification.png) |  ![](images/heater_failure_notification.png)

### Understanding the Menus

- Menu Legend

![Menu Legend](images/menu_icons.png)

- General App Info is contained in the upper right Hamburger Menu.

Main App Hamburger Menu Location              |  Main App General Info
:--------------------------------------------:|:------------------------------------------------:
![](images/hamburger_menu_location.png)   |  ![](images/main_app_info_1.png)

[Back](../)
