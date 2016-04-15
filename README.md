DH Drone D1 acro firmware
work in progress - was working but have not flown last version

_currently waiting for new board_

###notes
* acro only , level mode not functional
* protocols bayang (H8) and CG023
* programming requires vcc (3.3) wire.
* board may need power cycle after initial erase

###Compiling:
Compile using MDK-ARM toolchain aka Keil uVision. A special version is available for stm32F0xx devices ( full free version ), but it's not necessary since the 32K limit of the free version is above the cpu's 16K. STM32 support may need to be installed using the "pack installer" 

###Radio protocol:
Current options are stock cg023 transmitter or H8 mini transmitter / devo. I recommend using the H8 protocol with Devo tx, as the cg protocol only allows approx 7 bits accuracy. Protocol is by default stock CG023 protocol.


###Differences from H8 version:
 * rates have been integrated into protocol file, and depend on protocol abilities
 * the quadcopter rate ( in deg/sec) is no longer multiplied by 2, so it's the actual rate with devo.
 * linux version compiles above 16K, so it's not included.
 * acro only version can be compiled by enabling respective setting in config.h

###Installation and Support
Currently this port is covered by the H8 thread on rcgroups. Flashing is similar, except STM support is added using the pack installer. The programming port needs 4 wires ( 3.3V ). Battery warning may be incorrect while flashing.
http://www.rcgroups.com/forums/showthread.php?t=2512604 _H8 thread_

http://www.rcgroups.com/forums/showthread.php?t=2634611#post34381034 _CG023 thread_

###History:

###Board images:

https://github.com/silver13/d1/blob/master/img/d1-board-bottom.jpg

https://github.com/silver13/d1/blob/master/img/d1-board-top.jpg

![Board image](/img/d1-board-bottom.jpg)

![Board image](/img/d1-board-top.jpg)



