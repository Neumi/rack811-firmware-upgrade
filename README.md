# rack811-firmware-upgrade


1. get the firmware
choose from here https://www.rakwireless.com/en/download/LoRa/RAK811#Firmware_Upgrade

  OR

``` sh
curl https://github.com/RAKWireless/RAK811_BreakBoard/blob/master/bin/rak811_tracker_classA.bin --output 
rak811_tracker_classA.bin

```

2. get the RIGHT stm32flash code and make

``` sh
git clone https://github.com/Ebiroll/RAK811_BreakBoard/tree/master/stm32flash_src
cd RAK811_BreakBoard/tree/master/stm32flash_src
make
```

3. flashing the rak811
``` sh
cd RAK811_BreakBoard/tree/master/stm32flash_src
./stm32flash -w /PATH/TO/FIRMWARE/FILE/rak811_tracker_classA.bin /dev/tty.SLAB_USBtoUART
```


