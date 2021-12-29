#### [User Guide](user_guides) &nbsp;&nbsp;&nbsp;&nbsp;[Video Guides](user_guides/video_guides.md) &nbsp;&nbsp;&nbsp;&nbsp;[SDI-12 Info](sdi12_info) &nbsp;&nbsp;&nbsp;&nbsp;[Data Sheet](data_sheet/SNOdar_Data_Sheet.pdf) &nbsp;&nbsp;&nbsp;&nbsp;[Field Data](field_data_WY2021) &nbsp;&nbsp;&nbsp;&nbsp;[Latest Firmware Release](https://github.com/SensorLogicInc/snodar-releases/releases) &nbsp;&nbsp;&nbsp;&nbsp;[Privacy Policy](privacy-policy)

<p href="https://github.com/SensorLogicInc/snodar-releases/releases" align="center" style="color:red;font-size:18px;"> Major Firmware Update v0.7.0 + App Update v0.4.0 as of 12-22-2021 (see Changelog)! </p>

# SNOdar Snow Depth Sensor from Bozeman, Montana

&nbsp; 

<p align="center">
  <a href="https://sensorlogicinc.github.io/snodar-releases/"><img src="assets/images/sli_logo.png" style="width:25%" /></a>
</p>

&nbsp; 

## Product Overview: Available for Purchase [Here](https://sensorlogic.store/collections/snow-science-instrumentation/products/snodar-snow-depth-sensor)
SensorLogic's new SNOdar sensor is used for accurately and robustly monitoring snow depth and new snowfall in remote sensing applications, even during winter storm events.

<p align="center">
<b>Accuracy + Low Power + Low Cost!</b>
</p>

SNOdar measures seasonal snow depth and snowfall. Simultaneously, it can relay data over a serial RS-232 or SDI-12 bus to commercially available telemetry, i.e. Satcom, data logger, or cell modem. Moreover, it can record an entire season of data on its internal, nonvolatile data logger so there is no need to pair every sensor with a separate data logger;therefore, a large cost savings upon deployment. 

<p align="center">
  <a href="https://sensorlogicinc.github.io/snodar-releases/"><img src="assets/images/splashscreen.png" style="width:30%" /></a>
</p>

The sensor is small and lightweight, yet durable enough to monitor snow depth all season long at -40 degC and colder. The unit is typically powered from +12 VDC battery source and consumes less than 0.5 Watt on average. A small battery and solar panel (e.g. 50Ah + 10W) is all that is needed for seasonal deployment, depending on lattitude. The unit can be set up to operate as a distance sensor, stormboard snowfall sensor, or a seasonal snow depth sensor. A powerful mobile App allows the user to quickly configure and deploy the unit as well as monitor real-time data when within Bluetooth range. As a stormboard sensor, view or download the latest storm snow total, wipe the board, and re-calibrate for the next snowfall event. Furthermore, within minutes of deployment set up the unit as a standalone depth/snowfall sensor and data logger. Return periodically with an App-enable mobile device to download the latest data and instantly upload the data to a cloud platform, of your choice, for viewing, management, or analysis.

### Get the latest Mobile App:
 
<p align="middle">
  <a href="https://play.google.com/store/apps/details?id=com.snodar"><img src="assets/images/google-play-badge.png" width="350" /></a>
  <a href="https://apps.apple.com/us/app/snodar/id1584974884"><img src="assets/images/apple-app-store-badge.png" width="350" /></a> 
</p>

## Applications

- SNOTEL Snow Depth Monitoring
- Stormboard Snowfall Measurement
- Avalanche Monitoring and Forecasting
- DOT Road Conditions Monitoring
- Ski Resort Snow Monitoring
- Cornice Growth
- General Snow Management

## Features

- Real-time, accurate snow depth information during storms and heavy snowfall (NO postprocessing necessary)
- Bluetooth Low Energy (BLE) enabled configuration, installation, and live display
- Seasonal internal data logger
- Seasonal snow depth and new snowfall, even during heavy snowfall
- Seasonal snowfall totals
- Model-based Snow Water Equivalent (SWE) (*upgrade, coming soon!)
- SDI-12 data logger connectivity with commercially available devices (e.g. CSI CR6)
- RS-232 Satcom connectivity with commercially available devices (e.g. Rockblock Iridium)
- Sensor orientation monitoring (e.g. high snow load, high wind, tower shifting)
- Normal or oblique angle mounting (up to 30 degrees) for flexible mounting locations on inclines or stormboards
- Low power deployment, &le; 500 mW average consumption

## Specifications

| Parameter             | Sub-Parameter Description                                                      | Min      | Max      | Units         |
| --------------------- | ------------------------------------------------------------------------------ | -------- | -------- | ------------- |
| Input Voltage         | Input voltage range (VDC)                                                      | 6        | 24       | volts         |
| Operating Temperature | Outside, ambient operating temperature range                                   | -40      | 60       | °C            |
| Storage Temperature   | Inside, ambient storage temperature range                                      | -40      | 85       | °C            |
| Mechanical Vibration  | Mil-STD-883D, Method 2007.2, 20 to 2000 Hz                                     |          | 20       | g             |
| Mechanical Shock      | Mil-STD-883D, Method 2002.3, 1 msec, 1/2 sine, mounted                         |          | 500      | g             |
| Ingress Protection    | Dust tight. Immersion, up to 1 meter depth                                     | IP67     |          |               |
| Corrosion Resistance  | MIL-A-8625, Aluminum anodizing process (6061 T6)                               | Type II  |          |               |
|                       |                                                                                |          |          |               |
| Accuracy              | Typical deviation from absolute depth                                          | +- 1     | +- 2     | cm            |
| Resolution            | Minimum detectable depth change                                                | 0.3      | 1        | cm            |
| Range                 | Distance from snow target                                                      | 0.09     | 9        | meters        |
| Measurement Interval  | 1 minute granularity                                                           | 1        | 60       | minutes       |
|                       |                                                                                |          |          |               |
| Current Consumption   | @ 12 VDC, with Heater ON                                                       | 0.250    | 0.260    | amps          |
| Current Consumption   | @ 12 VDC, with Heater OFF (Idle, Active)                                       | 0.035    | 0.045    | amps          |
| Power Consumption     | Max measured with heater ON                                                    | 0.42     | 3.2      | watts         |
| Average Power         | Typical average seasonal power usage                                           | 0.5      |          | watts         |
|                       |                                                                                |          |          |               |
| Weight                | Without and with mounting clamp, respectively                                  | 265      | 375      | grams         |
| Size                  | 6.3 x 6.3 x 9.5 (W x L x H)                                                    |          |          | cm            |
| Obliqueness           | From vertical, angle slant relative to measuring surface                       | -30      | 30       | degrees       |

## Electrical Interfaces

### Wired

The communication standards accessible on cable allow for rapid deployment with commercial off-the-shelf (COTS) telemetry devices. 
- 1 RS-232 port (common among commercial Satcom / LTE modems)
- 1 [SDI-12 port](sdi12_info) (common among remote sensors and commerical data loggers)

### Wireless

#### Bluetooth Low Energy (BLE) 5.x

- 2 Mbps PHY capable, up to 50 meters Line-of-Sight (LOS)
- Long Range 125 Kbps PHY, up to 250 meters LOS
- The wireless connection allows for quick setup and calibration, data monitoring and sharing.

## Accessories

### Cable

The cable that ships with the SNOdar has a straight overmolded connector. 
  - Rated -40°C to 105°C
 - Power Rating: 300V
 - IP67 Connector (Outer Jacket is UV and Water Resistant)
 - Wire Gauge: 20 AWG
 - UL Recognized, CSA Certified and RoHS Compliant
 - Length: 10 meters
 - Blunt cut for connection flexibility

The [cable pinout](user_guides) and [cable data sheet](data_sheet/5C8070_CD.pdf).

### Mounting Clamp

The clamp that ships with the SNOdar is aluminum 6061-T6 with 304-stainless steel hardware and accommodates a pipe OD of 1.49-1.58". Please contact SLI if a different size clamp is required.
 - Medium duty clamp for 1.5" OD Tube
 - Minimum Tube Size: 38mm 
 - Maximum Tube Size: 40mm
 - Maximum Load Capacity: 100kg/220lbs

The [clamp drawing](data_sheet/CJS5001(40)AS.pdf), a custom derivative of this pn: [MINI 360 1.5](https://www.globaltruss.com/mini-360-1-5).

## Regulatory Compliance & Certs

### Full Compliance

- EMC
  - [x] FCC 15B and ISES-003 Issue 7
  - [x] CISPR 32:2015 / CENELEC EN 55032:2015
  - [x] CISPR 35:2016 / CENELEC EN 55035:2017
  - [x] ETSI EN 301 489-1 v2.2.3:2019
  - [x] ETSI EN 301 489-17 v3.1.1:2020
- IP67
  - [x] IEC 60529 Section 13.4, 13.6
  - [x] IEC 60529 Section 14.2.7
- Safety
    - [x] IEC 61010-1:2010
    - [x] IEC 61010-1:2010/AMD1:2016
- [x] RoHS

## Folder Structure

```
├── data_sheet
│   ├── SNOdar_Data_Sheet.pdf           # Main PDF data sheet
├── field_data_WY2021
│   ├── README.md                       # Info on field data sites
│   ├── BannerSummitSNOdarWY2021.png    # Data PNG
│   ├── BogusBasinSNOdarWY2021.png      # Data PNG
│   ├── BridgerBowlSNOdarWY2021.png     # Data PNG
├── privacy-policy
│   ├── README.md                       # Privacy policy markdown file
├── sdi12_info
│   ├── README.md                       # Basic information on the SDI-12 interface and data
│   ├── 1_minute_9_values.CR1X          # Logger program for CR1000X data loggers
│   ├── 1_minute_9_values.cr6           # Logger program for CR6 data loggers
├── user_guides
│   ├── README.md                       # Quick Start Guide on the SNOdar sensor and setup via the mobile App
│   └── images                          # Contains the images for this markdown file
```

**[Home](https://www.sensorlogic.ai/)**
