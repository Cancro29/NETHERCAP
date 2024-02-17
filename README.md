# NETHERCAP
A Wi-Fi penetration and social engineering tool for ESP8266 and ESP-32.Contact at nethercap.dev@gmail.com

## 21-01-2024 Announcement
NETHERCAP for ESP8266 is now free to use. Go to https://github.com/Cancro29/NETHERCAP/releases/tag/ESP8266 to download

## About this Project
This firmware is a heavily-modified version of M1z23R's ESP8266-EvilTwin v2.
It supports both ESP8266 and ESP-32. For now, ESP8266 build only supports Indonesian Language.
I will add more languages if requested.

## Password
The default password for "NETHERCAP" is "deauther".

## Features (Some features are missing on ESP-32 build because it still in development)
- Evil-Twin : Customizable HTML page with a custom fake "loading/reconnecting" page.
- Deauth All : Deauth all targets in range. Target get refreshed every 60 seconds.
- Multi-target deauth : Choose more than one target to deauth.
- Rogue AP  : Create a fake login page that asks for user's credential.
- Auto-resume : Continue operation even after the module gets restarted unintentionally.
- Monitor Page : Monitor and record status and events.
- Logger  : Record the events that happened during usage.
- Customizable : Modify some settings, and the settings will stay persistent.
- Sniffing : Count how many users connected to an AP.
- Extender : Connect an AP and then extend it using different AP name.
- File Manager : Upload, choose custom HTML page, or flash firmware in one menu.
- HTML Menu : Choose a custom HTML. You will get the preview so you can see what the target will see.
- OLED support : Display status. Currently only capable of showing in 64x48 resolution.

## How to use
- Flash the .bin file using your favorite flasher.For ESP-32 build, please read readme first. 
- Connect to "NETHERCAP" Access Point.
- Wait for captive portal to appear or access 192.168.4.1 on your browser.
