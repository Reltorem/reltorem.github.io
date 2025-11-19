---
layout: post
title: "OSI, TCP/IP Model and IP Intro"
date: 2025-11-14 12:00:00 +1000
categories: networking
---
**The OSI Model**


OSI stands for Open Systems Interconnection.
It's a theoretical reference model that maps the various layers or stages involved in sending data through a network.
It is helpful in teaching and understanding networks and data transfer.
You can use the analogy of sending post through the postal network and grouping the various layers it goes through - initial receive, sorting, transporting, delivering, etc.
Generally speaking, there are 7 layers, but sometimes less are involved.

They are:

- Application - The point where the application interfaces with the network.

- Presentation - Where the data is formatted, encoded, compressed etc.

- Session - Connections are managed and kept track of.

- Transport - Data is broken into chunks and delivered (protocols: TCP/UDP).

- Network - Finds the best path, deals with routing and protocols like IP addresses.

- Data Link - Deals with error detection and protocols like MAC addresses.

- Physical - The step involving physical hardware like cables, switches and devices.

They go in that specific sequence, although there may be some overlap among groups.
You can use a mnemonic to remember them such as top-to-bottom:

All
People
Seem
To
Need
Dad
Pants

Or bottom-to-top:

Please
Do
Not
Throw
Away
Sausage
Pizza

**TCP/IP Model**


Whereas the OSI model is more of a theoretical framework used for understanding network systems, the TCP/IP (Internet Protocol Suite) is the practical model that the internet is actually built on and defines specific protocols.

It is condensed to 4 layers:

- Application (User-level communication)
- Transport (End-to-end communication)
- Internet (Logical addressing and routing)
- Network Access (Physical transmission on local networks)

As data travels down through each layer, it is **encapsulated** - wrapped with headers or trailers that add information needed to get the data to where it needs to go. Different protocols are responsible at different layers. The data is **decapsulated** as it moves back up.

E.g.
- Application layer creates data (HTTP request).
- Transport layer adds header and wraps it in a TCP **segment** (adds source/destination ports)
- Internet layer wraps that in an IP **packet** (adds source/destination IP addresses).
- Network Access layer wraps that in an ethernet/WiFi **frame** (Adds MAC addresses and trailer)

Upon arrival at the destination, the data is unwrapped, or 'decapsulated' in reverse and the payload data is delivered to the correct place.


**Common Protocols**

**TCP (Transmission Control Protocol)**

- Transport layer protocol.
This is encapsulated by the IP protocol.
One of two main transport protocols along with UDP.

- Connection-oriented: This means there is a formal connection setup and close.
TCP is 'reliable' delivery as it checks to make sure the data actually arrived correctly, can recover from errors and manage transmissions out of order.

- Slower, but useful if you want to ensure data is all sent properly.

**Common Communications Using TCP**


- HTTPS (Hyper Text Transfer Protocol Secure)

Application layer protocol.
TCP transport (port 443)
This is HTTP that is encrypted.

- SSH (Secure Shell)

Application layer protocol.
TCP transport (port 22)
Used for secure encrypted remote login and command execution.


**UDP (User Datagram Protocol)**


- Transport layer protocol.
This is encapsulated by the IP protocol.
One of two main transport protocols along with TCP.

- Connectionless: No formal connection setup and close.
'Unreliable' delivery: No acknowledgement from receiving device. It just sends the data.
No error recovery. Can't handle out of order messages or retransmissions.
Often the application can handle data that doesn't get through and will decide what to do about it.

- Faster, useful if you just want to quickly send data and a few errors don't matter - e.g. streaming, real-time communication.


**Common Communications using UDP**


- DHCP (Dynamic Host Configuration Protocol)

Application layer.
Connectionless protocol, transport works alongside UDP (port 67/68)
This works as a pool of IP addresses that can be assigned or temporarily 'leased' to devices in a network.

- TFTP (Trivial File Transfer Protocol)

Application layer.
Connectionless protocol, transport works alongside UDP (port 69)
Used for lightweight file transfer like network booting, firmware loading.


