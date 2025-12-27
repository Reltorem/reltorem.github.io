---
layout: post
title: "Project: Laptop Battery Replacement"
date: 2025-12-26 12:00:00 +1000
categories: [projects, hardware]
---
**Laptop Faulty Battery Replacement**


**Aim**
- Diagnose and repair/replace faulty battery in laptop.

**Tools**
- Phillips-head screwdriver
- Anti-static wrist strap
- Spudger
- Tweezers

**Diagnosis and Procedure**
- Observed laptop battery would occasionally drop from near-full to completely empty in a matter of seconds and turn off. Overall battery life appears much shorter than when the laptop was new.
- Laptop is about 5 years old and so degraded battery performance would be expected.
- Confirmed by generating a battery report using command: 'powercfg /batteryreport'
- Battery report indicated the design capacity to be *43,000 mWh* and full-charge capacity to be around *23,000 mWh* or less - a capacity reduction of almost 50%. This indicates the battery can no longer function adequately and needs to be replaced.
- Replaced the battery with the following procedure:


**1.**
- Source a genuine ASUS OEM replacement battery. Confirm model number: *B31N1637*. Confirm voltage rating is the same or equivalent: *11.52V*
- Wear anti-static strap and ensure it is grounded properly.
- Remove laptop backcover, store removed screws carefully so each can go back into it's original location.

<img src="\images\battery-replacement\oem-battery.jpg" alt="a picture of a new ASUS battery pack." style="width:auto; height:200px;">


**2.**
- Using a spudger, disconnect the battery from the motherboard by sliding back the lock and pulling the connector up.

<img src="\images\battery-replacement\disconnect-battery.jpg" alt="a picture of disconnecting the battery pack." style="width:auto; height:200px;">


**3.**
- Using Philips-head screwdriver, unscrew the WLAN adaptor and carefully disconnect from the motherboard.
- Unthread the antennae cables so they're free from the battery

<img src="\images\battery-replacement\disconnect-WLAN-adaptor.jpg" alt="a picture of disconnecting the WLAN adaptor." style="width:auto; height:200px;">


**4.**
- Remove battery and dispose of it safely according to local regulations.
- Replace with new battery.
- Rethread WiFi antennae cables, reconnect WLAN adaptor to motherboard and reconnect new battery to motherboard. Replace laptop backcover.


**5.**
- Ensure new battery works by turning on laptop.
- Deplete battery to ~10%, fully charge and generate new battery report.
- Confirm full-charge capacity meets design-capacity.

<img src="\images\battery-replacement\battery-report.png" alt="a screenshot of battery report showing improved charge capacity." style="width:auto; height:200px;">


----


**Results**
- The faulty component was replaced succesfully.
- The laptop's battery life is now similar to when it was new.
- The battery no longer rapidly discharges or dies without notice.

**Conclusion**
This repair demonstrated the successful diagnosis of a common computer issue and the execution of a routine procedure in the IT support industry. Approprate steps were taken in handling components safely, such as correctly using an anti-static wrist strap, disconnecting the battery before dealing with other components and carefully tracking/organsing removed screws and parts.