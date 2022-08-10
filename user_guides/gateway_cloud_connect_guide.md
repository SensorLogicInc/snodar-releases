# SNOdar Chairlift Gateway ([SNOCHGW](https://sensorlogic.ai/sensor-products/SNOdar-Chairlift-Gateway)) + SNOdar Cloud Connection Guide

[Back](../)

> **Purchase on our web shop: [SNOdar + Chairlift Gateway Bundle](https://sensorlogic.store/collections/snow-science-instrumentation/products/snodar-chairlift-gateway?variant=42569883025563)**


## Dependencies

- SNOdar Firmware: [snodar-v0.8.0](https://github.com/SensorLogicInc/snodar-releases/releases/tag/0.8.0-beta) or later (see [SNOdar DFU](https://www.youtube.com/embed/v8IoPYJle9w) to first update the SNOdar's firmware)
- Mobile App: `SNOdar Snow Depth v0.4.6` or later (update this in your mobile app store of choice)

Play Store App                                                                                  |  iOS App Store
:----------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:
[![](../assets/images/google-play-badge.png)](https://play.google.com/store/apps/details?id=com.snodar)   | [![](../assets/images/apple-app-store-badge.png)](https://apps.apple.com/us/app/snodar/id1584974884)

## Hardware Setup

### __---Power and Boot Gateway__

1. Unbox and attach the 6-pin power cable to the main connector. The connection is directionally keyed. Make sure to engage the bayonet locking mechanism. 

Chairlift Gateway            |  Power Connection                     
:---------------------------:|:------------------------------:
![](images/snochgw.jpg)      |  ![](images/snochgw_power.jpg)  

2. Supply 6-24 VDC (0.5W supply minimum is needed to support the LTE-M backhaul) to the cable leads according to the pinout below:

| SNOCHGW Pin Name| SNOCHGW Pin NO.| Cable Pin NO. |  Wire Color |
| --------------- | -------------- | ------------- | ----------- |
| GND             | 1              | 1             | BLACK       |
| PWR +12V        | 2              | 2             | WHITE       |
| GND             | 3              | 3             | GREEN       |
| (RES)           | 4              | 4             | RED         |
| (RES)           | 5              | 5             | BLUE        |
| (RES)           | 6              | 6             | VIOLET      |

> Note: **15 Watt** capable, or less, max power supply is required. When on battery supply, an inline fuse **MUST** be located close to the battery that limits the battery supply to 15W or less. For example:
- @ 12Vdc use a 1A fuse
- @ 24Vdc use a 0.5A fuse

### __---Connect to SNOdar__
 
1. Once powered, both LEDs will be __RED__ upon boot. 

> Note: If the SNOdar has already been [Provisioned](#snodar-provisioning), see below, The left LED (BLE Indicator) will turn __Blue__ once it connects to a valid SNOdar, with the greatest RSSI, via BLE and the right LED (LTE-M/LoRa Indicator) will turn __Green__ once it successfully connects to the LTE network in range.

2. Make sure the Gateway is in `Good` BLE signal range of the SNOdar, $\leq$ 20 meters.

3. Mount the Gateway on the SNOdar tower with [U-Bolts](https://www.mcmaster.com/u-bolts/center-to-center~1-1-2/thread-size~1-4-20/) or heavy-duty UV-resistant [Zipties](https://www.mcmaster.com/cable-ties/uv-protection~uv-resistant/width~0-23/width~0-22/width~0-2/width~0-19/minimum-temperature~-75-f/minimum-temperature~-65-f/minimum-temperature~-50-f/minimum-temperature~-40-f/). Typically, this can be below the SNOdar unit ~1 meter off the ground, depending on cell coverage. Unit(s) should be located outside for proper cell connectivity.

> Note: The BLE LED will be solid __Blue__ and LTE LED will be solid __Green__ when everything is connected and operational. 

## SNOdar Provisioning

### __---Dashboard Setup__

1. Provisioning the SNOdar with the [snodar.io](https://app.snodar.io/groups/) Cloud Service using the Mobile Link can be done independently of the Gateway backhaul unit; however, it is useful to have both units powered and operational so data can be verified on the [Dashboard](https://app.snodar.io/) once the steps are completed.

2. [`Sign In`](https://app.snodar.io/login?ref=%2F) to your account, or create a new account on the `snodar.io Dashboard`.

![](images/dashboard_signin.PNG)

3. Create a `Group` or navigate to an existing [`Group`](https://app.snodar.io/groups/) that you want to use for your SNOdar unit.

![](images/dashboard_groups.PNG)

4. Once the `Group` is created, click on the `<Group Name>`, then click `Link Mobile Device` to retrieve a provisiong code. Copy the code for later use in the [Mobile App](#mobile-app-setup).

![](images/dashboard_edit_group.PNG)

![](images/dashboard_link_mobile_device.PNG)

![](images/dasboard_link_code.PNG)

### __---Mobile App Setup__

1. Power the SNOdar sensor, according to the [User Guide](README.md), and start the Mobile App in your mobile device. Connect to the SNOdar unit via BLE.

![](images/mobile_connect.PNG)

2. Navigate to the main App `Settings` menu by using the [Hamburger Icon](images/hamburger_menu_location.png) in the upper right corner. Then activate the `Cloud Mobile Link` drop down and choose `+ Add a Group Code`.

![](images/mobile_link_dropdown.PNG)

3. Type in the `Group Code` you copied from `Link Mobile Device` on the web [Dashboard](https://app.snodar.io/) and hit `Submit`.

![](images/mobile_link_code.PNG)

4. Navigate back to the Mobile App `Home` page (you should still be connected to the desired SNOdar sensor) to `Register` the specific SNOdar and `Enable` the SNOLOG cloud upload, by toggling the [Cloud](images/cloud_disable_enable.png) icon.

5. Toggle the [Cloud](images/cloud_disable_enable.png) icon to `Register`, then toggle again to `Enable`.  The icon will turn from white (with a diagonal line) to green (with an arrow pointing up) and be enabled.

Toggle                                  |  Register                              | Toggle                                  | Enable                    
:--------------------------------------:|:--------------------------------------:|:---------------------------------------:|:--------------------------------------:
![](images/mobile_cloud_enable_1.PNG)   |  ![](images/mobile_cloud_register.PNG) |  ![](images/mobile_cloud_enable_1.PNG)) |  ![](images/mobile_cloud_enable_2.PNG)  

6. Finally, the [Cloud](images/cloud_disable_enable.png) icon will display as `Enabled`, indicating the Gateway is now uploading a SNOLOG from the desired SNOdar, based on the configured `Interval Time` requested in the [Setup Wizard](https://www.youtube.com/embed/s7zSW9LP-iM).

![](images/mobile_cloud_enabled.PNG)