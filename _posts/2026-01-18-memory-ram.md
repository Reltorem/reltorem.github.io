---
layout: post
title: "Memory/RAM"
date: 2026-01-18 12:00:00 +1000
categories: hardware
---
Broadly speaking there are two main types of memory - volatile and non-voltile.

Volatile (RAM)
- Not permanent, loses data when power is lost
- Fast
- Short-term working memory for active data

Non-volatile (Storage - SSD, HDD, flash)
- Permanent storage - data remains without power
- Slower
- Long-term storage

- Non-volatile memory like SSD or HDD can be thousands of times slower to access than RAM.
- Data therefore has to be loaded into RAM before it can be used by the computer.
- It's important to ensure your system has enough working memory to handle your needs.

**RAM (Random Access Memory)**

- Holds active programs and data
- Faster RAM generally means better system performance
- Results are often written back to storage after processing
- 64-bit data width - means memory moves data in 64-bit (8 byte) blocks at a time
- Random access means any memory location can be accessed instantly by address (as opposed to serially)

*Compatibility*

- RAM is not universally compatible
- Must match the motherboard's supported memory type
- Always check motherboard specs before upgrading

-

*Form Factors*

DIMM (Dual Inline Memory Module):

- Used in desktops
- 'Dual Inline' means electrical contacts run parallel  on both sides (different signals)
- Installed vertically straight into a DIMM slot on the motherboard

SO-DIMM (Small Outline DIMM):

- Used in laptops/mobile devices
- About half the size of a DIMM
- Installed at an angle, then locked flat

-

*Terms*

DRAM (Dynamic RAM) / SDRAM (Synchonous DRAM)
- Standard type of RAM in modern computers
- Dynamic means data is constantly refreshed (thousands of times/sec) to keep it in capacitors.
- Synchronous means memory is synchronised to a system clock
- Allows coordinated, predictable data transfer between CPU and memory

SRAM (Static RAM)
- Doesn't require constant refreshing
- Used for CPU cache, not main system memory

DDR (Double Data Rate) Memory
- All modern system RAM is DDR
- Transfers data twice per clock cycle (rising + falling edge)
- Doubles data throughput compared to single data rate memory

DDR2 -> DDR3 -> DDR4 -> DDR5 (current gen)

Each new generation:
- Higher speeds
- Often higher capacity per module
- Not backward compatible (Older memory cannot be used in newer motherboards, and vice versa)
- RAM modules have notches (keys) in different positions to prevent installing the wrong DDR generation into a motherboard

-

*Special Memory Types*

Standard RAM
- Basic computer memory

Parity Memory
- Adds extra parity bit per byte (so an extra ninth bit) to detect errors
- Detects errors but cannot correct them
- System may still crash or need a reboot when an error occurs
- Works by checking the byte for even parity

Example byte 1: 11100111 = 6 '1's. This is even. So we would add a parity bit of 0 to the end.

Example byte 2: 10011000 = 3 '1's. This is odd. So we would add a parity bit of 1 to the end.

When the data is retrieved, the parity is checked again, and a new parity bit is added to make the sequence even.
This new parity bit is then compared against the original parity bit in memory - if they match, the data is intact. If the bits are different, some error has occured with one of the bits in the byte.

E.g. - If example byte 1 is evaluated on retrieval and is found to be odd, a parity bit of 1 is added to make it even. That is then compared against the original bit which is 0, and the system knows that an error has occured and the data has changed in some way.

ECC (Error-Correcting Code) Memory:
- Can detect and also correct errors automatically
- Ensures system continues running normally (important for servers or critical services)
- Standard, Parity, and ECC modules all look similar physically

-

*Memory Bandwidth*
- Measures data transfer speed between CPU and RAM
- Expressed in MT/s (Million Transfers per second)
- E.g. DDR5-5600 performs 5,600 MT/s
- Bottlenecks and engineering physics limit transfer speeds in individual modules. 

Can increase throughput using *Multichannel Memory*
- Adding multiple channels allows CPU to access multiple RAM modules simultaneously
- Common configurations: dual-channel (most common), triple-channel, quad-channel
- Matching modules (same type, size, speed) improves performance
- Motherboards often color-code slots to indicate channel pairs
- Means 2x 16GB modules has the same total capacity as 1x 32GB module, but higher thoughput