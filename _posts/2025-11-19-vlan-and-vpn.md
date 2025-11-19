---
layout: post
title: "VLANs and VPNs"
date: 2025-11-19 12:00:00 +1000
categories: networking
---
**VLANs (Virtual Local Area Network)**


A *LAN* is a *Local Area Network*. This is a group of devices that are in the same broadcast domain.

Being in the same broadcast domain means they are connected together (either through a physical switch, or wirelessly - a WLAN) and are separated from other networks or segments of a larger network by different switches or a router.

If you have different networks on different switches however, it might be a much more efficient use of hardware to simply run several networks through the same switch.

In this case, the different networks can be configured as VLANs - Virtual Local Area Network. So everything runs through the same hardware but are still separated logically, not physically.

Some of the ethernet ports can be designated for network A, some can be designated network B, and so on.

As long as the switch is configured correctly, it should be very difficult for a bad actor to gain access to other networks.


**VPN (Virtual Private Network)**


A VPN encrypts all traffic within it so data cannot be intercepted.

A concentrator is responsible for encrypting and decrypting in real time, and is often integrated into a firewall.

It is often deployed as cryptographic hardware, especially in enterprise situations, but there are software-based concentrators available too.

VPN software can be easily installed on your phone or laptop. Another advantage of this is you can choose where your encrypted traffic is routed on the way to it's destination, so your traffic appears to originate from a proxy server in a different location.

*Client-to-site VPN* is often used by businesses for their remote users. VPN software will be installed on a remote users device and will likely be configured to be 'always-on'. They then connect to a VPN concentrator on the edge of a corporate network and send their encrypted traffic. The concentrator then decrypts the traffic and passes it through to access the resources within the corporate network.

*Site-to-site VPN* is similar, but securely connects two different sites. Site A will send unsecure traffic to a concentrator where it is encrypted and securely sent over the internet to the concentrator at site B, where it is decrypted again.

