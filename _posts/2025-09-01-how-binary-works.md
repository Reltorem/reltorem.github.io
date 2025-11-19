---
layout: post
title: "How Binary Works"
date: 2025-09-01 12:00:00 +1000
categories: networking
---
**Binary**


Binary is a base-2 numbering system that represents all values using only two symbols: 0 and 1. It is the 'language' spoken by computers.
Computers are essentially just number processing machines, but they process numbers a little differently to us.
As humans, we like to count in a decimal system, which is base-10. That just means there are 10 digits to work with: 0-9.
Imagine you are writing down numbers, counting upwards one at a time. You write 1 through to 9, then when you run out of digits you roll the column back to 0 and add 1 to a new column beside it. This way we can express infinite numbers using only 10 digits. Each time a column reaches 9, it rolls back to 0 and 1 is added on to the next column. This means each column is 10 times larger than the one before it.
Add the value of each column to get the total value.

For example, this is 325:

10M 1M 100k	10k	1k	100	10	1

0	0	0	0	0	3	2	5

Binary is the same, but is base-2, which just means you have 2 digits to work with, 0 - 1.
If you imagine counting upwards in the same manner, you add 1 and then you've already run out of digits. So the first column rolls back to 0 and you add 1 to the column beside it.
So 0000 0001 is 1, 0000 0010 is 2, and 0000 0011 is 3.
This means each column will be twice as large as the one before it.
If you want to convert a binary value to decimal, just add up the columns as before:

128	64	32	16	8	4	2	1

0	0	0	1	0	1	1	0

This value 0001 0110 would be 22 (16 + 4 + 2 = 22).
A bit is one of these digits (0 or 1) and is the smallest unit of information a computer can process. To make it easier to manage as humans, we like to think of bits in groups of 8, which is called a byte.
Then 1,000 bytes make a kilobyte, 1,000 kilobytes make a megabyte, and so on. (Strictly speaking, it's actually 1,024 bytes in each since binary storage grows in powers of 2, but 1,000 is close enough).
So when writing numbers in binary, we write out the full 8 digits and if the number is too small, just add zeros in the larger columns like the example above.
The largest decimal number that can be expressed in 1 byte is therefore 255, because that would be 1111 1111 in binary.
As humans, we like using decimal because groups of 10s are easy to calculate, and probably also because we have 10 fingers and have used our hands to count since we first figured out what counting was.
Computers like binary, because all the information being processed by a computer or a network is physical.

To illustrate what this means, consider a CPU. The Central Processing Unit is the main 'brain' of the computer that does most of this processing. If you zoom into a CPU microchip, you will find a thin silicon wafer about the size of your thumb nail, printed with billions upon billions of nanoscopic transistors. Each of these transistors is essentially just a simple switch. They can be in one of two states: ON or OFF, which the computer reads as 1 or 0. The state of the transistor can be switched by passing a voltage through it.
So if you wanted to convey to a computer the number 15 you might switch a row of transistors to OFF, OFF, OFF, OFF, ON, ON, ON, ON.
As the computer scans through the row of switches and reads their states, it sees 0000 1111 which is binary for 15.
(In reality this isn't quite accurate because a bit is actually represented by multiple transistors working together and CPUs are very complicated, but the general idea still holds conceptually).
If there are only 2 states to differentiate between, it is very clear cut - it's either OFF or ON. If each switch could be in one of 3 states (i.e. a trinary system) the computer would have to differentiate between low voltage, high voltage and an in-between medium voltage on each transistor which is more subtle and much more error prone, especially when you consider that billions of these switches are involved, processing billions of calculations a second. It's also more complicated and expensive to engineer.

When information is sent through a network, it often is sent via optic cabling. The bits (0s and 1s) and translated and sent as pulses of light. It's much easier to read LIGHT ON (1) or LIGHT OFF (0) than having to differentiate between various levels of light intensity, becoming ever more subtle with the more states you add.

So even though expressing information in binary may seem inefficient as it can easily blow out into extremely long strings of 0s and 1s to express even a tiny piece of information, it is simple, reliable and allows a computer to process vast amounts of information with excellent precision.
Theoretically, a base-10 system or larger would be better and more efficient because we could express more information with 1 bit, but from an engineering perspective, it's practically impossible.

Side note: Russian computer scientists actually experimented with building trinary computer systems in the 80s, which meant each transistor could be set to one of 3 voltage levels, but even just accurately defining 3 states was a pain to engineer and it resulted in too many errors to be viable.
