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

<p>
  <img src="img/mUCA_Base_top.svg" alt="drawing" width="450"/>
  <img src="img/mUCA_Ant_bottom.svg" alt="drawing" width="450"/>
</p>
