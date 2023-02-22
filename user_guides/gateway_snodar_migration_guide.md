# SNOdar + Chairlift Gateway Migration Guide to [SNOfire Chairlift Dashboard](chairlift.snofire.io)

[Back](../)

> ### **Purchase on our web shop: [SNOdar + Chairlift Gateway Bundle](https://sensorlogic.store/collections/snow-science-instrumentation/products/snodar-chairlift-gateway?variant=42569883025563)**

## Dependencies

- SNOdar Firmware: [snodar-v0.9.4](https://github.com/SensorLogicInc/snodar-releases/releases/tag/0.9.4-beta) to force update
- SNOdar Firmware: [snodar-v1.0.0](https://www.dropbox.com/s/lmt0zs7a14w5snn/snodar_secure_dfu_esb_v1.0.0.zip?dl=1) to migrate to new dashboard
- Mobile App: `SNOdar Snow Depth v0.4.6` or later (update this in your mobile app store of choice)

Google Play Store App                                                                                  |  iOS App Store
:----------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:
[![](../assets/images/google-play-badge.png)](https://play.google.com/store/apps/details?id=com.snodar)   | [![](../assets/images/apple-app-store-badge.png)](https://apps.apple.com/us/app/snodar/id1584974884)

## Natural SNOdar Firmware Update via Mobile App

_1. Get within Bluetooth range of both the SNOdar and Gateway units ($\leq 20$ meters).

_2. Connect to the SNOdar using the Mobile App

_3. Check for the latest updates and update naturally, using the FW update dropdown, to the most current cloud released firmware: [snodar-v0.9.4](https://github.com/SensorLogicInc/snodar-releases/releases/tag/0.9.4-beta)

![](images/dfu_check_update.png)

_4. Once this has rebooted, reconnect via the BT mobile app and Force Gateway Firmware Update.

## Force Gateway Firmware Update

_1. Click on the white `Cloud Icon` and a message appears to either `Register` or `Enable`.

![](images/mobile_cloud_enable_1.PNG)

_2. Click the `Register` button to force the Gateway to upgrade firmware. This will allow the Gateway to access the new server endpoint and download the latest firmware.

> Note:  
> Ignore any old functionality alerts about an "active group link key" or "Cloud Mobile Link"

![](images/mobile_cloud_register.PNG)

_3. Watch the Gateway LEDs, as the BLE LED will breifly go Cyan then turn Magenta while it is downloading firmware. The download will take 4-78 minutes. If it is successful the unit will reboot itself, so both LEDs will turn off then come up as RED. The LTE LED should go Green in less than 30 seconds. 

_4. If the unit immediately reboots after initiating this process or the LEDs both turn Yellow (Watchdog Reset), try Steps 1-3 again until it is successful.

_5. When successfull, set the Serial Number and Cloud Enable.

## Set Serial Number to Provision SNOdar and Cloud Enable

_1. You must rename the SNOdar in the App to the given Serial Number on the bottom of the unit next to the QR code. The SN will be a 6-digit number with the following format: `210<xxx>`.

_2. Again, open the specific SNOdar and navigate to the `Config` page.

![](images/view_toolbar_config.png)

_3. Choose the `Sensor` dropdown then `Name` and type in the 6-digit serial number from the bottom of the unit. Hit `Save`.

![](images/view_config_name.png)

_4. Next, toggle the Cloud Icon button again and choose `Enable` so data will be automatically send to the cloud database.

![](images/mobile_cloud_enable_2.PNG)

The Cloud Icon will turn Green.

![](images/cloud_disable_enable.png)

_5. Finally, reboot the unit, and then do a Manual SNOdar FW Update

![](images/snodar_restart.PNG)

## Manual SNOdar Firmware Update via Mobile App

_1. Download the new SNOdar FW [snodar-v1.0.0](https://www.dropbox.com/s/lmt0zs7a14w5snn/snodar_secure_dfu_esb_v1.0.0.zip?dl=1) to your mobile device. 

> Note:   
> Some devices require you to rename the firmware file before it can be visible by the Mobile App when choosing the file

_2. Start the Mobile app and connect to the SNOdar. Open the specific SNOdar and navigate to the `Config` page.

![](images/view_toolbar_config.png)

_3. Under `Actions` dropdown choose `Manual Firmware Update` then choose the v1.0.0 FW file you downloaded in Step 1.

![](images/fw_manual_update.png)

_4. Let this process complete, the SNOdar will reboot and flash Green.

_5. Reconnect to the SNOdar over Bluetooth with the Mobile App and Claim the Serial Number in the new Dashboard.

## Claim Serial Number on new [Dashboard](chairlift.snofire.io)

_1. Navigate to the [Chairlift Dashboard](chairlift.snofire.io) and log in to your account (or Create an Account)

_2. Navigate to the `Legacy: Claim a SNOdar` page, see the left side nav bar.

![](images/legacy_claim_snodar.png)

_3. Enter the 6-digit Serial Number and hit `Go`.

![](images/legacy_claim_snodar_go.png)

_4. Your SNOdar should be claimed and viewable on the new Dashboard within 24 hours.