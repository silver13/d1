##DH Drone D1 acro firmware##

*acro only*

Please check board images are similar before flashing, 2 variations exist

###notes
* acro only , level mode not functional
* programming requires vcc (3.3) wire.
* board may need power cycle after initial erase
* I now use a diode (1n4148) to drop voltage from 3.3V. I programmed the quad without it a number of times. ymmv

###Compiling:
Compile using MDK-ARM toolchain aka Keil uVision. A special version is available for stm32F0xx devices ( full free version ), but it's not necessary since the 32K limit of the free version is above the cpu's 16K. STM32 support may need to be installed using the "pack installer" 

###Radio protocol:
Options of bayang ( H8 ) bayang plus ( made up, sends pids to quad from tx ) cg023, CX-10 blue ( original protocol of this quad) and H7
Bayang plus is backwards compatible with bayang protocol. Note, currently set to bayang default, not cx-10.


###Differences from H8 version:
 * rates have been integrated into protocol files, and depend on protocol abilities
 * the quadcopter rate ( in deg/sec) is no longer multiplied by 2, so it's the actual rate with devo.


###Installation and Support
Currently this port is covered by the H8 thread on rcgroups. Flashing is similar, except STM support is added using the pack installer. The programming port needs 4 wires ( 3.3V ). Low battery warning may be incorrect while powered via st-link.
http://www.rcgroups.com/forums/showthread.php?t=2512604 _H8 thread_
or
http://www.rcgroups.com/forums/showthread.php?t=2634611#post34381034 _CG023 thread_

###History:

###Board images:

https://github.com/silver13/d1/blob/master/img/d1-board-bottom.jpg

https://github.com/silver13/d1/blob/master/img/d1-board-top.jpg

![Board image](/img/d1-board-bottom.jpg)

![Board image](/img/d1-board-top.jpg)

![programming](/img/sch1.jpg)



