# ONVIF Device Discovery Tool

A tool to scan your local network and discover ONVIF-compliant devices (IP cameras, NVRs, etc.). The tool attempts to authenticate and retrieve device metadata using common credentials.

## Features

- Automatic LAN scanning for ONVIF devices
- Device authentication testing
- Retrieval of RTSP stream URLs
- Device metadata collection

### Usage

Requires Node.js 18 or higher.

```shell
npx onvif-probe@latest --login try:password --login another:credential
```

### Example output

```
NVT (urn:uuid:de9b935e-5566-7788-99aa-0012314ae65b)
 └─ http://192.168.1.30:8899/onvif/device_service
   └─ <empty>:<empty>
   └─ rtsp://192.168.1.30:554/user=admin_password=tlJwpbo6_channel=0_stream=0.sdp?real_stream
   └─ rtsp://192.168.1.30:554/user=admin_password=tlJwpbo6_channel=0_stream=1.sdp?real_stream

Reception (urn:uuid:3132c01c-b794-4c4a-97f3-f023b9532d83)
 └─ http://192.168.1.120:80/onvif/device_service
   └─ admin:admin
   └─ rtsp://192.168.1.120:554/live/main
   └─ rtsp://192.168.1.120:554/live/sub
```
