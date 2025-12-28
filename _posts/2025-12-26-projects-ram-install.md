---
layout: post
title: "Project: Laptop RAM Installation"
date: 2025-12-26 12:00:00 +1000
categories: [projects, hardware]
---
**Laptop RAM Installation**


**Aim**
- Upgrade the memory capacity in laptop from 8GB to 16GB by installing new RAM module.

**Tools**
- Phillips-head screwdriver
- Anti-static wrist strap

**Diagnosis and Procedure**
- Laptop has 8GB of preinstalled memory and was running near full capacity with a few tabs open in Chrome.
- Running complex workloads and multiple plugins in a DAW sometimes resulted in hang-ups.
- Resource monitor indicates a high number of hard faults/sec, indicating the system is running out of RAM and paging heavily.
- I noticed there is an empty RAM slot that can be utilised, so I decided to fill it and double the laptop's memory capacity to 16GB with the following procedure:


**1.**
- Use a software tool like CPU-Z to determine what RAM is currently installed and then source a good quality RAM module with the same specs.

The original memory module has the following specs:

- **SO-DIMM**: Form factor is *Small Outline-Dual Inline Memory Module*. This is a smaller laptop form factor of standard DIMM. Dual-Inline means two parallel rows of contacts on opposite sides of the module.
- **8GB**: Capacity of the module is 8GB.
- **DDR4**: 4th gen. speeds. Still current, but now being replaced by newer DDR5. DDR 'Double Data Rate' means it sends a signal twice per clock cycle.
- **2400 mHz (1200 mhz)**: Frequency of how many times data is transferred per second. Because it's DDR, the actual base speed is half of the effective rate (which is usually what is advertised). Adding a new RAM module that's faster won't help because the system will bring it back down to the slowest RAM module. I used a module of identical speed to avoid any potential compatibility or performance issues to be safe.
- **1.2V**: Electrical power supplied to the RAM. Must be the same.
- **SK Hynix**: The manufacturer. SK Hynix is a reputable memory brand. The new stick I bought happened to be the same brand, but it doesn't necessarily need to be.

<img src="\images\ram-installation\cpuz-slot1.png" alt="A CPU-Z screenshot showing the specs of the original RAM module." style="width:auto; height:200px;">


**2.**
- Confirm there is an empty usable RAM slot on the motherboard.

<img src="\images\ram-installation\empty-slot.jpg" alt="An image showing an empty RAM slot next to the exisiting filled RAM slot." style="width:auto; height:200px;">


**3.**
- Disconnect battery as an extra safety precaution to avoid damaging any components. Unlock the connector and carefully pull it up.

<img src="\images\ram-installation\disconnect-battery.jpg" alt="A picture of disconnecting the battery pack." style="width:auto; height:200px;">


**4.**
- With an earthed anti-static wrist band on, line up the RAM module with the guide slots and carefully push it in horizonally and down, until the locking mechanism slides into place.

<img src="\images\ram-installation\install-ram.jpg" alt="A picture of installing the new RAM stick." style="width:auto; height:200px;">


**5.**
- Reconnect battery and replace laptop back cover.
- Quickly ensure the computer recognises the new RAM by booting into the BIOS menu and confirming how much installed memory is being registered.
- Run CPU-Z again to inspect the specs of the new RAM stick.
- Run some tasks and check Resource Monitor/Task Manager to ensure that RAM usage is no longer being maxed out.

<img src="\images\ram-installation\ram-bios.jpg" alt="A picture of BIOS screen showing the amount of installed memory." style="width:auto; height:200px;">

<img src="\images\ram-installation\cpuz-slot3.png" alt="A screenshot of the software CPU-Z displaying the specs of the newly installed RAM module." style="width:auto; height:200px;">


----


**Results**
- The new RAM module was installed successfully.
- The laptop no longer runs out of memory or hangs when running usual workloads.

**Conclusion**
This installation demonstrated an understanding of RAM and it's specifications. It also demonstrated the successful execution of a common and basic procedure in IT support work. Approprate steps were taken in handling components safely, such as correctly using an anti-static wrist strap, disconnecting the battery before dealing with other components and carefully tracking/organsing removed screws and parts.