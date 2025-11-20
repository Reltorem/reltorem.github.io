---
layout: post
title: "Network Devices"
date: 2025-11-20 12:00:00 +1000
categories: [networking, hardware]
---
**Common Network Devices & Hardware**

These are some of the most common pieces of hardware you might find in a server room or somewhere on the network:


**NIC (Network Interface Card)**

- Fundamental component that lets a device communicate on a network.
- Translates data into signals that can be carried over a network.
- Often built into the motherboard, but could also be an expansion card.
- Specific to network type and capabilities (Ethernet, WAN, wireless, etc.)
- Implements MAC addressing.


**Routers**

- Routers route traffic between subnets.
- They connect different network types and infrastructures too: LAN, WAN, copper, fibre, etc.
- Routers operate at Internet layer in TCP/IP model or OSI layer 3 (Network).
- Often they are integrated with a switch. These would then be known as *layer 3 switches* or *multi-layer switches*. Switches otherwise operate on OSI layer 2 (Data Link).


**Switches**

- A switch is a hardware bridge that connects devices in a LAN and forwards traffic based on MAC addresses.
- Central to an enterprise network.
- The switching itself is done on hardware like an ASIC (Application-Specific Intergrated Circuit). This makes it fast enough to keep up with high-speed LAN traffic.
- Often has many ports and integrated features.
- Some switches may also provide power through the ports in addition to data (PoE - Power Over Ethernet).
- Many switches also have routing functionality.

**Unmanaged Switches** are very simple and are essentially plug-n-play. They typically have limited numbers of ports and do not feature many (or any) configuration and management options or additional functionality, like multiple VLANs.
- They just connect some devices together in a LAN, and that's about it. Sometimes this is all you need, and this simplicity also makes them cheaper.

**Managed Switches** are required in enterprise settings. They are larger, offering more ports and interfaces.
They can be configured and managed remotely and feature additional functionality such as:
- VLANs.
- Traffic prioritisation (Like giving voice traffic high priority).
- Redundancy support to maintain uptime.
- Packet monitoring and *port mirroring*.


**PoE (Power over Ethernet)**

- Power provided over an ethernet cable along with data.
- Useful for phones, security cameras and difficult-to-power areas.
- Many switches provide PoE themselves (This power from the source switch is known as Endspan). PoE switch ports are usually clearly labelled.
- Otherwise, an *injector* can be installed (known as Midspan). An injector connects an ethernet cable and a switch, but is also plugged into it's own power supply to 'inject' power in the middle.

There are several generations:

- PoE: 15.4 W, 350 mA max current.
- PoE+: 25.5 W, 600 mA max.
- PoE++: 51 W, 600 mA (type3) / 71.3 W, 960 mA (type 4)

These generations are not upwards compatible, so check switch support before installing.


**Access Point**

- Not a wireless router, just a bridge extending wired to wireless and vice-versa.
- Makes forwarding decisions based on MAC addresses.
- A router is actually an access point and a router in one device.
- Might look like a small dome installed on a wall or ceiling.


**Cabling Infrastructure**

- In an office, ethernet cables typically run from each workstation into the network cabinet/room and are locked down in a *punch-down* block on the **patch panel**.

- You could theoretically just plug all desks directly into a switch, but making the cable run from desk to patch panel permanent and bringing everything together to one central point makes everything more reliable and easier to manage and organise.

- So the patch panel typically has permanent punch-down blocks on one side, and *RJ-45 connectors* on the other side. Connections can be labled, making it easy to match up which cable goes to which desk.

- On the other side of the patch panel, connections can then be easily and reliably moved around or changed - perhaps to plug a user into a different switch, to replace a bad cable, or to change the switches themselves.


**Firewalls**

- Generally filters traffic by TCP/UDP port number.
- Compares the traffic against a set of pre-configured rules to decide whether to allow the traffic or not.
- More modern firewalls can filter by application/type of traffic instead of port e.g. it might allow web traffic, but block remote access applications.
- Can also contain VPN concentrator, allowing you to encrypt/decrypt traffic passing through it.
- Can act as a traffic proxy for security, analysing traffic before passing it through to the user.
- Most firewalls can also be used as a router.


**Cable Modem**

 - A cable modem allows your network to communicate with your ISP via the *coaxial cable* used by cable TV.
- Translates high frequency RF signals from the coax cable to standard digital ethernet frames your computer or router can understand.
- It does this using *DOCSIS (Data Over Cable Service Interface Specification)*.


**DSL (Digital Subscriber Line) Modem**

- A DSL modem allows your network to communicate with your ISP via *telephone lines*.
- Speeds decrease with distance from the central office (CO), up to a functional limit of about 3km.


**ONT (Optical Network Terminal)**


- This allows fibre to the premises (FttP). It translates communications from fibre to copper.
- It is a demarcation (demarc) point separating the private network and the ISP infrastructure. The 'outer' side is the responsibility of the ISP, and the 'inner' side is the responsibility of the premise.
- In fibre to the node (FttN), the fibre cabling runs to a shared central node out in the street somewhere, then copper runs to each premise. In this case, you would not need an ONT.