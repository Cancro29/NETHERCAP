## How to Activate 5 GHz Support on NETHERCAP 2.7
To make 5 GHz deauther working on NETHERCAP 2.7, you need :
1. Wemos D1 Mini with NETHERCAP 2.7 installed.
2. BW16 RTL8720dn board which looked like this : %BW16%
3. USB to TTL adapter
4. Arduino IDE version 1.8.XX with Realtek Ameba Boards (32-bits ARM Cortex-M33@200MHz) version 3.1.4 installed.
5. Amebad ImageTool v2.3.2
6. NETHERCAP Lite firmware for BW16 RTL8720dn
7. Soldering skill
8. Jumper cables
9. Breadboard (optional)

## Before Starting
In general, there are 4 steps to flash BW16 RTL8720dn board:
1. Connect BW16 to USB to TTL
2. Erase OTA firmware from BW16
3. Flash NETHERCAP Lite
4. Connect RX and TX wire to both BW16 and Wemos D1 Mini

Please read carefully before proceeding. I don't answer obvious questions. This tutorial is all I know and I can't answer questions beyond that.
# 1. Connect BW16 to USB to TTL
BW16   -> USB Serial Adapter
LOG_RX -> TX
LOG_TX -> RX
3V3    -> 3V3
GND    -> GND

After that. Trigger BW16 to enter download mode by doing this :
1. Connect LOG_TX to GND
2. Connect EN to GND and then reconnect EN to 3V3 to trigger reset
3. disconnect LOG_TX from GND
4. BW16 now entered download mode

# 2. Erase OTA firmware from BW16
1. Open Arduino IDE, click on "Tools" and set "Erase Flash" to "Enable"
%IMG_BW16_setErase%
2. Click "Upload" button. It is okay to upload empty sketch.
%IMG_BW16_erase%
3. If it erased successfully. Arduino log should looked like this:
%IMG_BW16_eraseSuccess%

4. Open Arduino Serial monitor
5. Reset the board by touching EN pin to GND pin and then disconnect it.
6. If you see "#calibrate OK", you can proceed. If not, you're out of luck as I don't know how to fix this.
7. Trigger BW16 to enter download mode again for flashing.

# 3. Flash NETHERCAP Lite
First, download NETHERCAP Lite here : %LINK%
%IMG_BW16_ImageTool%
1. Open Amebad ImageTool v2.3.2, click "CHIP SELECT" on top left corner, then click "AmebaD(8721D)"
2. Choose the COM port to USB to TTL you are using.
3. Make sure the baud rate is 1500000
4. Check the fourth check box
5. Click "Browse" and select NETHERCAP Lite firmware. Make sure the Address is set to "0x08006000"
6. Click "Download"

If flashing is successfull, the flash log should looked like this : 
%IMG_BW16_flash_success%

7. Reset the board by touching EN pin to GND pin and disconnect it.
8. An AP named "NETHERCAP_5GHZ" should appear
9. To double check, open Arduino Serial monitor and do step #7 again, a series of debug message should appear

# 4. Connect RX and TX wire to both BW16 and Wemos D1 Mini
BW16   -> Wemos D1 Mini
PB2    -> TX
PB1    -> RX
3V3    -> 3V3
GND    -> GND

*note  : I haven't tried powering BW16 by attaching 3V3 and GND to Wemos D1 Mini. Try using USB to TTL's 3V3 and GND first

1. Power on both board and wait for 20 seconds
2. Open NETHERCAP SoftAP that comes from Wemos D1 Mini. Do not connect to "NETHERCAP_5GHZ"
3. A secondary table that contains 5 GHz networks should appear on target list.
%IMG_esp8266_5ghz%
