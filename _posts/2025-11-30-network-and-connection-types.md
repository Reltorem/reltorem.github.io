---
layout: post
title: "Internet Connection and Network Types"
date: 2025-11-30 12:00:00 +1000
categories: networking
---
**Internet Connection Types**


There are different ways of physically connecting to the internet. Some of the most common include:

**Satellite**
- Non-terrestrial communication.
- Higher cost relative to terrestrial networking.
- Good for remote sites/lacking infrastructure.
- Higher latency (potentially ~250ms up/down, but could be more like ~60ms up/down).
- Weather and geography can negatively affect signal.

**Fibre**
- Slightly more expensive than copper to install and repair.
- High speed transmissions.
- Long distance.
- FttN or FttP is now common around Australia.

**Cable**
- Runs over coaxial cables like the ones used for delivering television to a premise.
- Broadband (Carries wide range of frequencies).
- Supports different traffic types - Voice, Data, Video, etc.
- Operation defined by DOCSIS (Data Over Cable Service Interface Specification).

**ADSL/DSL (Asymmetric / Digital Subscriber Line)**
- Runs over copper phone lines
- Asymmetric means download speed is faster than upload (By 10x could be expected)
- Has a maximum range of about 3km and speeds will slow as you get further from the CO (Central Office).

**Cellular Networks**
- Uses the mobile phone tower network
- You can often *tether* a device (like a laptop) directly to a mobile device with cellular internet (like a phone) and use it as a *hotspot*.
- Dedicated mobile internet dongles perform this same function.

**WISP (Wireless Internet Service Provider)**
- Terrestrial internet connection that is broadcast wirelessly to multiple networks.
- More common in rural or remote areas.
- It's like a giant central WiFi router - Often looks like a central antennae in the street that different networks can connect to via 802.11 (WiFI), 5G, or some proprietary wireless technology.


**Network Types**


There are many different network types, based on their size or scope. The most common network types include:

**PAN (Personal Area Network)**
- Bluetooth, Personal devices like earphones, Car entertainment, etc.

**LAN (Local Area Network)**
- Usually a building or group of buildings.
- High speed direct connection - Ethernet and 802.11 wireless.

**WLAN (Wireless LAN)**
- A wireless LAN running on 802.11 wireless technologies (WiFI).

**MAN (Metropolitan Area Network)**
- Network that encompasses a whole city, town or suburb.
- Usually state owned and managed infrastructure.

**WAN (Wide Area Network)**
- Scope is global.
- Generally connects multiple LANs.
- Usually much slower than a LAN due to a lack of direct connectivity.
- Systems like *Point-to-point serial* or *MPLS (Multiprotocol Label Switching)* can be used to connect LANs more directly and reliably over public infrastructure.
- The internet itself could be called a WAN.

**SAN (Storage Area Network)**
- Storage often on an isolated network but connected to the main network with a very high speed connection.
- Looks just like a local storage device to other network hosts.
- Block-level access - Fast and efficient read/write.


