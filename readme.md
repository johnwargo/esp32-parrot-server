# ESP32 Parrot Server

A simple web server sketch for ESP32 devices that returns an HTTP 200 response code and information about the request to the calling device/application.

## Background

While working on an application for a Wi-Fi enabled device, I realized I needed a server for the application to connect to as I tested the device. I didn't have the target hardware lying around that I needed, so I decided to create this sketch to allow me to test the app's connectivity while I waited for the final hardware.

## Configuring the Sketch

Copy the repositories `config.h.rename` file to `config.h`. This file contains the configuration settings for the sketch. By separating the configuration values into an external file that's not part of the repository, I can publish updates to the sketch and you'll be able to download them without overriding the configuration settings with the default values from the repository.

Modify the contents of the configuration file for your particular needs:

```c
#define WIFI_SSID "MyLocalNetwork"
#define WIFI_PASSWORD "my long and complicated Wi-Fi password"

#define HOSTNAME "parrot"
```

| Config Setting  | Description |
| --------------- | ----------- |
| `WIFI_SSID`     | The Wi-Fi network name (SSID) you want the sketch to connect to. |
| `WIFI_PASSWORD` | The password for the Wi-Fi network SSID specified in `WIFI_SSID` |
| `HOSTNAME`      | The network name for the ESP32 Parrot server.  |

## Operation

To use the server, configure 


```text
***********************
* ESP32 Parrot Server * 
* By John M. Wargo.   * 
***********************

Connecting to MyLocalNetwork
..
WiFi connected
IP address: 192.168.86.88

Web server: MDNS responder started
Web server: HTTP server started
Web server: Request: /someRequest
```