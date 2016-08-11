Adafruit_MCP9808
================

This is the Adafruit MCP9808 Precision I2C Temperature sensor library

Tested and works great with the Aadafruit MCP9808 Breakout Board 
    ------> http://www.adafruit.com/products/1782

This chip uses I2C to communicate, 2 pins are required to interface

Adafruit invests time and resources providing this open source code, 
please support Adafruit and open-source hardware by purchasing 
products from Adafruit!

Written by Kevin Townsend/Limor Fried for Adafruit Industries.  
BSD license, check license.txt for more information
All text above must be included in any redistribution

To download. click the DOWNLOADS button in the top right corner, rename the uncompressed folder Adafruit_MCP9808. Check that the Adafruit_MCP9808 folder contains Adafruit_MCP9808.cpp and Adafruit_MCP9808.h

Place the Adafruit_MCP9808 library folder your arduinosketchfolder/libraries/ folder. You may need to create the libraries subfolder if its your first library. Restart the IDE.


MF - Add resolution support 
===========================

void write_resolution(uint8_t resolution);

tempsensor.write_resultion(1)

Resolution bits
00 = +0.5°C (tCONV = 30 ms typical)
01 = +0.25°C (tCONV = 65 ms typical)
10 = +0.125°C (tCONV = 130 ms typical)
11 = +0.0625°C (power-up default, tCONV = 250 ms typical)

uint8_t read_resolution();

Serial.println(tempsensor.read_resolution(),BIN);