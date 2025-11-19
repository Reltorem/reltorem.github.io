---
layout: post
title: "IP Addressing - IPv4 & Subnets"
date: 2025-09-02 12:00:00 +1000
categories: networking
---
**IPv4**


What I learned:
How IPv4 addresses are structured and how subnetting works in detail.

Why it's valuable:
IP protocol and subnetting is foundational knowledge in understanding networks. Networks are a crucial part of IT work, so it's important to understand how they work and how to troubleshoot them.


An IP (Internet Protocol) address is a unique code that identifies a device within a network.
IPv4 looks like 4 sets of numbers separated by dots, e.g. 192.168.1.0
Each set of numbers is called an octet because it's made of 8 bits. Therefore, there are 32 bits in the whole IPv4 address.

In binary, the IP address 192.168.1.0 mentioned above is:
11000000.10101000.00000001.00000000

The crucial thing to remember is that although we write these numbers in decimal, because it makes it easier for us to understand as humans, computer systems are reading it in binary. So it's important to interpret the numbers in 2 'languages' at the same time.
The address contains two pieces of information: The network the device belongs to, and the specific host device within that network.
The portion identifying the network is on the left and the host portion is on the right.

A CIDR (Classless Inter-Domain Routing) prefix is attached to the address to indicate the subnet mask, which defines which part of the address is the network and which part is the host.
We add CIDR notation to the end of the IP address to indicate the prefix length which looks like /x, with x being a value between 1 and 32.
e.g. 192.168.1.0 /24
The subnet mask defines which bit marks the boundary between network and host.

In this case (/24) it's 255.255.255.0
11111111.11111111.11111111.00000000

The bits that are 1s are the network, and the bits that are 0 are for the host.
The network bits are fixed and must be consecutive - all the 1s of the subnet mask are grouped on the left and those bits in the IP address cannot be changed.
There are multiple host devices on the network however, so the host bits can change to represent every device in the network.


Host bits can also be 'borrowed' and allocated to the network in order to further subnet or subdivide the network into smaller subnets. The total number of possible hosts remains roughly the same (minus 2 for each new address block for the broadcast and network addresses), but they are just grouped into smaller subnets to help with organisation.
As an example, if you have a prefix of /24 and then borrow an extra 2 host bits from the fourth octet to subnet the network to /26, you have made 4 new blocks in the last octet:

00xx xxxx
01xx xxxx
10xx xxxx
11xx xxxx

So the blocks in this case increment by 64 and can start from 0, 64, 128 & 192.
The first possible address in each block is reserved for the network address. This can't be used as a host address because it identifies the subnet itself.
The last possible address in each block is reserved for the broadcast address. This can't be used as a host address either because this is the address that devices use when they want to message all devices on the their network.
So you have to subtract 2 addresses from each subnet to know the total number of usable addresses in that subnet.

