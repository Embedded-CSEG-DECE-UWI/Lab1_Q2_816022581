# Lab1_Q2_816022581
Repository for ECNG 3006 Lab 1 Q2. I love the esp, it has enriched my life and broadened the narrow horizon that was once my prior understanding of suffering. I have never been happier!

#Lab2_P1
1. File: /project/sdkconfig
This is an automatically generated file which is the ESP-IDF project configuration settings. 
A large amount of configuration settings are commented out as 'not set' in this file. 
The information that remains includes the settings that were selected in make menuconfig, such as the flashing mode (in this case dout), and the flashing frequency (40M). 

2. File: /project/build/include/sdkconfig.h
This is an automatically generated file which is the ESP-IDF configuration header. 
It includes much of the same information from the above file but it is #defined and presented in the format of a header file. 
It also only includes the set configuration fields and does not include the non-set fields or comments from the above file. 
This includes what is needed for configuration of the build.
It incldues information such as the monitor baud rate (74880), the port for flashing the esp (in my case, it is /dev/ttyUSB0), the esp flashsize (1MB is the setting that I used to flash my esp), the flashing mode (dout) and other confiuration settings for the idf.  

3. File: /sdk/components/freertos/port/esp8266/include/freertos/FreeRTOSConfig.h

This is the freertos configuration file which specifies how freertos is configured on the esp8266. 
The default configuration values can be overwritten, such as is done in Lab2 Q2 to enable pre-emption. 
If the contents of this file were to be changed then the behavior of the system would be altered. 
A specific example of this would be in line 104 of the above file, if this value were changed from 1 to 0, then vTaskDelay would not be able to be used in the program.
