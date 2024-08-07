# NETHERCAP
A full-featured Wi-Fi penetration and social engineering tool for ESP8266 and ESP-32.Contact at nethercap.dev@gmail.com

Like this project? Consider giving a star to this repo, I will appreciate that.
# Untuk Pengguna di Negara Indonesia
Mohon untuk tidak membeli produk NETHERCAP dari toko daring di bawah ini, karena mereka melakukan tindakan kurang etis terhadap konsumen/developer.<br>
Jika bisa, berikan rating paling rendah pada produk terkait. Apabila sudah terlanjur memberikan rating, laporkan toko/produk tersebut dengan alasan "Menjual produk dilarang lainnya"
![Scheme](images/shopee1.PNG)

# 5 GHz Deauther
5 GHz deauther for BW16 RTL8720dn is currently in development. Stay tuned!
Proof : https://github.com/Cancro29/NETHERCAP/blob/main/images/IMG_20240721_065236.jpg <br><br>

# Help Needed!
Need someone who can find a way to flash compiled firmware into BW16 RTL8720dn board. If you know how to do it, please contact me via email.
# Download
## ESP8266
https://github.com/Cancro29/NETHERCAP/releases/tag/V.2.6-esp8266
## ESP-32
https://github.com/Cancro29/NETHERCAP/releases/tag/ESP-32

## About this Project
This firmware is a heavily-modified version of M1z23R's ESP8266-EvilTwin v2 with Spacehuhn's Deauther CSS.
It supports both ESP8266 and ESP-32. For now, it supports English,Indonesian, and custom language.

## Password
The default password for "NETHERCAP" is "deauther".
## Pin and Control Scheme
![Scheme](images/NETHERCAP_quickguide.png)
## Features (Some features are missing on ESP-32 build because it still in development)
- Evil-Twin : Customizable HTML page with a custom fake "loading/reconnecting" page.
- Deauth All : Deauth all targets in range.
- Multi-target deauth : Choose more than one target to deauth.
- Rogue AP  : Create a fake login page that asks for user's credential.
- Auto-resume : Continue operation even after the module gets restarted unintentionally.
- Monitor Page : Monitor and record status and events.
- Logger  : Record the events that happened during usage.
- Customizable : Set your own settings and it will stay persistent.
- Sniffing : Count how many users connected to an AP.
- Extender : Connect an AP and then extend it using different AP name.
- File Manager : Upload, choose custom HTML page, or flash firmware in one menu.
- HTML Menu : Choose a custom HTML. You will get the preview so you can see what the target will see.
- OLED support : Display status. Currently only capable of showing in 64x48 resolution.

## How to use
- Flash the .bin file using your favorite flasher.For ESP-32 build, please read the instructions first. 
- Connect to "NETHERCAP" Access Point.
- Wait for captive portal to appear or access 192.168.4.1 on your browser.
