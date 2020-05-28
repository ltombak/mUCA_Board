# mUCA Board
> A developpment board based on the stm32WB and Semtech LR1110 with up to 9 antennas to test multi canals propagations.

[![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org)
![madewith](https://img.shields.io/badge/made%20with-KiCad-blue)


## Description
This is a board that use the new LR110 chip from Semtech (see https://www.semtech.com/products/wireless-rf/lora-transceivers/lr1110) and the STM32WB (see https://www.st.com/en/microcontrollers-microprocessors/stm32wb-series.html).

The main goal of this developpment board is to see how we can improve the range of IoT devices in differents environements using the right (low-cost) antenna.
To do that, we incroporated multiple antenna one the same PCB:
  - A *classic* 868 MHz IFA antenna.
  - A Circular Polarization Antenna, designed by Fabien Ferrero.
  - A u.Fl port to have the possibility to connect an external antenna.

Another purpose for this board is to test the new LR1110 which is a LoRa modem capable of GNSS fix with ultra low power consumption.
The implemented antennas are :
  - A GNSS IFA antenna.
  - A Circular Polarization GNSS ceramic patch antenna.
  - A 2.4 GHz IFA antenna (used for wifi sniffing by the LR1110).
  - A u.Fl port to have the possibility to connect an external antenna.


## How it's made
To lower the costs and the complexity, we designed two 2-layers boards: one with the circuitry and one with all of the antennas. The two boards are assembled with simple headers pins to connect them.

Here is a preview of the "Base" PCB and the "Ant" PCB:

<p>
  <img src="img/mUCA_Base_top.svg" alt="drawing" width="450"/>
  <img src="img/mUCA_Ant_bottom.svg" alt="drawing" width="450"/>
</p>

## TO-DO List
- [x] 1. Finishing Schematic
- [x] 2. Finishing Layout
- [x] 3. Generate BOM
- [x] 4. Order components
- [x] 5. Order PCBs
- [x] 6. Create placement document
- [x] 7. Assemble the boards
- [ ] 8. Program the GPIO of the mcu
- [ ] 9. Test the whole board (LEDs, Sensors, SPI links)
- [ ] 10. Test the radiation of the onboard antennas
- [ ] 11. Create the code to automatically choose which port to use on the CP Antennas (see below)
- [ ] 12. Test LoRa Transmission in real environements
- [ ] 13. Test GNSS power consumption with real case usage
- [ ] 14. Publishing the results.

## Timeline
| Event                         | Date          |
| ----------------------------- | ------------- |
| Project Start                 | 21 Feb 2020   |
| Schematic Complete            | 13 Mar 2020   |
| Layout Complete               | 27 Mar 2020   |
| Layout Correction             | 06 Apr 2020   |
| BOM Complete                  | 06 Apr 2020   |
| Ordered Components            | 10 Apr 2020   |
| Sent PCB to fabhouse          | 13 Apr 2020   |
| PCBs Received                 | 15 May 2020   |
| first assembly                | 22 May 2020   |

## Onboard sensors
Two sensors are presents on the PCB :
  - One Accelerometer
  - One BME280

With the accelerometer we can determine the orientation of the device and then choose the polarization to maximize the range of the device.
The BME280 (Temp/Humidity/Pressure) is just for testing.
