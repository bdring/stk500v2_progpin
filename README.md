#stk500v2_progpin

This is a minor mofification to the stk500v2 bootloader that shipped with the 1.6.6 Arduino.cc IDE.

The feature allows you to use a switch on a pin to put the bootloader into a mode where it permanently waits 
for the firmware upload.  This can be used when you cannot use a DTR reset or a power cycle is not practical.

Simply power on the device with the prog_pin connected to ground.  The switch can be released after power on without affecting this feature.

The pin used is PORTK Bit 2.  This can be changed in stk500boot.c.  All code is within #ifdef USE_PROG_PIN preprocessor directives.