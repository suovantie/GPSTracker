# GPSTracker
This system collects the location of moving devices, draws tracks to the map, works as a log book, where the user can white comments 
and collect photos.

This system consists of mobile devices with GPS, which sen data to a server through a mobile router.
The mobile devices are built around ESP32 and ESP8266 processor modules.
I have used here Wemos (Lolin) Mini D1 ESP32 and Wemos (Lolin) Mini D1 ESP8266, but any other modules can be used.

The trackers send their data through a router. I have used so called 2G/2G/4G/5G WiFi modems and Android phones, which can share the Wifi.

The data is collected in the server. So far I have used our home server.
The data comes as simple TCP packets, which have a key telling the device, which have sent the packet. 
The same program, which receives the packets from the trackers, accepts data also from any other device, which can send data to the TCP port.
The data is collected to normal linear files.

In the server there is a program, which views a table of the trip days. The cells contain tools to view the map and view and edit the text and pictures

Version 301026
