---
layout: post
title: "Network Cabling"
date: 2025-12-02 12:00:00 +1000
categories: [networking, hardware]
---
**Network Cables and Ethernet**

Ethernet is a protocol and family of standards defined by the IEEE (Institute of Electrical and Electronics Engineers). It defines how signals are sent and processsed in a network.
It can run over *twisted pair, coaxial or fibre*. TP is by far the most common and coaxial is essentially obsolete.

*Twisted Pair (TP)*
- Copper wiring
- Most common network cabling in homes and offices.
- Cables: Cat5e, Cat6, Cat6a, Cat7
- Connectors: RJ45
- Speeds: 10 Mbps - 10Gbps (10Gb possible over Cat6+)

*Fibre*
- Pulses of light
- Used in data centres, long-distance connections and high-speed data
- Speeds: 100 Mbps - 400Gbps+
- Connectors: LC, SC, ST
- Immune to EMI

*Coaxial*
- Copper wiring
- Early Ethernet standards used coax. Largely obsolete for Ethernet now.
- Speeds: 10 Mbps


**Twisted pair copper cabling**

- Multiple sets of colour-coded wire pairs twisted together.
- Each wire in a pair carries equal and opposite signals.
- Cabling signals are subject to random interference and noise from the environment, adjacent components and other wires.
- Twisting ensures that each wire in the pair has equal exposure to any source of interference so the 'noise' in each wire is effectively equal.
- To determine the real signal from the noise, the receiving end compares the difference in the two signals. Because the noise is virtually equal in each, it cancels out.

Example:

- The desired signal being sent on the cable is 2.0V
- Wire 1: +1V (+0.3V noise) = +1.3V
- Wire 2: -1V (+0.3V noise) = -0.7V
- 1.3V - (-0.7V) = 2.0V
- The receiving end interprets a signal of 2.0V

-*Sheilding*-

These twisted pair cables can be shielded or unshielded. The shielding protects the cable from EMI (ElectroMagnetic Interference)

- **UTP (Unshielded Twisted Pair)** - Most common TP cabling.
- **STP (Shielded Twisted Pair)** - Requires the cable to be grounded.

AOther abreviations (printed on cable jacket):

- (Overall cable) / (Individual pairs)TP

- U = Unshielded
- S = Braided shielding
- F = Foil shielding

E.g.

- S/FTP = Braided shielding around entire cable. Foil shielding on individual TPs.
- F/UTP = Foil sheilding around entire cable. Unshielded TPs.


**Coaxial copper cabling**

- Name comes from two components sharing a common axis:
- Copper wire conductor runs through the centre.
- Outer shielding runs along the outside of the inner wire core.
- Used to be a common Ethernet medium, but now mostly seen on cable modems.
- Also used for information other than networking, like television.


**Other special TP cabling**

Direct burial STP
- Designed to be directly buried without a conduit.
- Waterproof, strong, may be less flexible.
- May contain waterproof gel surrounding wires.
- Often contains a ground wire or *drain wire*.

Plenum-rated cable
- Plenum is the active air space above a drop roof.
- Cabling in this space must be fire-rated for safety.
- Cable jacket is made from FEP or low-smoke PVC.
- Traditional cable jackets are just regular PVC.
- Plenum-rated cable may be less flexible.


**Cable Categories**

When sending signals through copper cables, the cable itself has to be manufactured to a minimum standard (category) to support the type of signal that is required.

- These standards or cable categories are created by the IEEE.
- Consult the IEEE 802.3 (Ethernet) standards to determine what cable category you require for a particular system.

- 1 Gigabit Ethernet is still pretty much the standard in homes and offices.
- Speed: 1Gbps (1,000 Mbps)
- IEEE Shorthand: **1000BASE-T** (*1000*Mbps-*BASE*BAND-*T*wisted pair)
- Minimum cable category: **Cat. 5e** (Cat. 5 is older obsolete standard)
- Max cable distance: 100m

- 10 Gigabit Ethernet is more common in enterprise backbones, data centres and server rooms.
- Speed: 10Gpbs (10,000 Mbps)
- IEEE Shorthand: **10GBASE-T**
- Minimum cable category: Cat6
- Max cable distance: 55m UTP Cat6, 100m STP Cat6, 100m Cat6A

Homes and offices will typically use speeds of 1Gbps or 10Gbps.
- They will therefore use copper TP categories Cat5e, Cat6, Cat6a & Cat7.
- Cat8 is used for high speeds (25 - 40 Gbps) over short distances (max 30m) and so is typically only found connecting components in data centres or server rooms.





