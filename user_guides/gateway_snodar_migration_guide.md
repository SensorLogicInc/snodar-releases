# SNOdar Chairlift Gateway ([SNOCHGW](https://sensorlogic.ai/sensor-products/SNOdar-Chairlift-Gateway)) Migration Guide to [SNOfire](chairlift.snofire.io)

[Back](../)

> ### **Purchase on our web shop: [SNOdar + Chairlift Gateway Bundle](https://sensorlogic.store/collections/snow-science-instrumentation/products/snodar-chairlift-gateway?variant=42569883025563)**


## Dependencies

- SNOdar Firmware: [snodar-v0.9.3](https://github.com/SensorLogicInc/snodar-releases/releases/tag/0.9.3-beta) to force update
- SNOdar Firmware: [snodar-v0.9.9](https://www.dropbox.com/s/fqua6vbl91s1koj/snodar_secure_dfu_v0.9.9.zip?dl=1) to migrate to new dashboard
- Mobile App: `SNOdar Snow Depth v0.4.6` or later (update this in your mobile app store of choice)

Google Play Store App                                                                                  |  iOS App Store
:----------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:
[![](../assets/images/google-play-badge.png)](https://play.google.com/store/apps/details?id=com.snodar)   | [![](../assets/images/apple-app-store-badge.png)](https://apps.apple.com/us/app/snodar/id1584974884)

## Natural SNOdar Firmware Update via Mobile App

1. Get within Bluetooth range of both the SNOdar and Gateway units ($\leq 20$ meters).
2. Connect to the SNOdar using the Mobile App
3. Check for the latest updates and update naturally to the most current cloud released firmware: [snodar-v0.9.3](https://github.com/SensorLogicInc/snodar-releases/releases/tag/0.9.3-beta)
4. Once this has rebooted, reconnect via the BT mobile app and __Force Gateway Firmware Update__

## Force Gateway Firmware Update

1. Turn `On` Developer options in the main Settings Menu
2. Navigate to the `UART` tab in the Sensor `View`
3. Create two custom NUS commands to send to the SNOdar

### NUS Commands

- !FW,45.56.85.243
- !FWX

## Manual SNOdar Firmware Update via Mobile App

- v0.9.9

### Set Serial Number to Provision

### Claim Serial Number on new [Dashboard](chairlift.snofire.io)


## Troubleshooting FAQ

1. What if?