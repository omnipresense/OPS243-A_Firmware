# OPS243-A_Firmware
Latest hex file for OPS243-A radar sensor.
See application note AN-13 for the detailed steps to update the code using XMCFlasher and Segger programmer.
Do not use this hex file for OPS243-C.  Contact us for that code file.
This code file is for the XMC4500 based OPS243.  If you have the OPS243-A with the XMC4700 processor, contact us.

Changes from v1.3.2 include new timestamp message when the speed trigger is tripped and a high signal on GPIO4_0 (pin 1, J3 header) which will stay high until the Rolling Buffer sampling has completed.  Use the going high and going low signal to sync a camera or other device to the time period the data was sampled.  New SPnnn command is available to set time period auto-reset of Rolling Buffer.  Default is off and Rolling Buffer must be restarted with GC or PA commands.  Setting SPnnn with nnn in seconds from 0 to 600 enables Rolling Buffer to automatically start again after nnn seconds.
