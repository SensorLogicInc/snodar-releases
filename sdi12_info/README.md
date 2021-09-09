# SDI-12 Information

SNOdar was developed against a [CR1000X Campbell Scientific Data Logger](https://www.campbellsci.com/cr1000x). 

- The program [1_minute_9_values.CR1X](1_minute_9_values.CR1X) was downloaded to the CR1000x data logger to log from the SNOdar using SDI-12.
- The program [1_minute_9_values.cr6](1_minute_9_values.cr6) was downloaded to the CR6 data logger to log from the SNOdar using SDI-12.

Both programs include variable names and units. They were created with the program [Short Cut](https://www.campbellsci.com/shortcut)

The 9 ordered values supplied over SDI-12 by the SNOdar in order are as follows:

```
// Sensor Data
1. System Current (mA)
2. System Voltage (V)
3. Internal Temperature (degs C)
4. Orientation Flag (0 = normal, roll = bit 2, pitch = bit 1, yaw = bit 0)
5. Heater Enable (0 = off, 1 = on)
6. PCB Temperature (degs C)
7. Distance (meters) (average over N measurements)

// DSP Data
8. Seasonal Snow Depth
9. Day-of-Year SWE (*currently NOT available, returns as -1)
```

SNOdar is sensitive to two standard SDI-12 Commands issued to SDI-12 address 0. The supplied CR1X program causes the CR1000X to use these two SDI-12 commands to pull data from the SNOdar. 
```
0M!
```
followed by
```
0D0!
```
The above mentioned 9 pieces of ASCII data will be returned on the SDI-12 line. 


