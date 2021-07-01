# Hackintosh-Opencore-Asus-ROG-B550-F
Hackintosh ROG STRIX B550-F / Ryzen 9 3900X / RX570

I'm using this config for 4 months now, it is super stable. 

## Specification

| **Component** | **Model** |
| ------------- | --------- |
| CPU | AMD Ryzen 9 3900X @ 3.8GHz |
| Motherboard | ASUS Rog Strix B550-F (Wi-Fi) |
| RAM | 32GB (2 x 16GB) Kingston HyperX FURY @ 3200MHz |
| Audio Chipset | ALC1220 |
| GPU1 | SAPPHIRE NITRO RX 570 4G in PCI slot 2|
| GPU2 | ASUS GTX1070 8G in PCI slot 1 (for Windows)|
| Lan |  Intel® I225-V 2.5Gb Ethernet |
| WiFi |  Fenvi T919 |
| OS Disk | Intel SSD Pro 1500 180GB |
| macOS | Big Sur 11.2.3 |

## What works

- Ethernet
- USB
- iMessage, FaceTime

## Not tested

- Embedded Audio
- NVMe (I have a Sabrent 1TB nvme, but I use it for Windows... I will test it soon)

## Known issues
- Virtualization - expected.
- Sleep is not working - Use Amphetamine app to prevent MacOS to sleep. 
- I disabled embedded Intel Wi-Fi card kext, because they were causing MacOS to crash, I bought Fenvi T919 (everything works - Handoff, Apple Watch unlock etc.)
- I was having issues with my USB Audio interface Behringer UMC202HD, audio was dropping occasionally.FIX: I restored my BIOS settings to default and now it's gone. 
- 
- iMessage and FaceTime were not working. After many tries I called Apple Support, but there was not a problem with my Apple ID and they not found anything... so I tried one more time and it worked. This is my fix:
  -  See and remember all steps from Dortania's Fixing iServices guide (MAC/ROM section, en0!)
  -  Changed SMBIOS from iMacPro1,1 to MacPro7,1. 
  -  Generate new SMBIOS, I used a serial number which in apple's checkcoverage was showing "We’re sorry, but this serial number isn’t valid" :) 
  -  I disconnected my wifi network, used an ethernet cable and connected my computer direcly to my ISP provider (without router, in that way my IP address is new)
  -  Clear all previous attempts /Dortania's Fixing iServices guide is your friend :)/

