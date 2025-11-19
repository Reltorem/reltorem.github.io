---
layout: post
title: "Network Services"
date: 2025-11-16 12:00:00 +1000
categories: networking
---
**Common Network Services**


There are a number of important services that are critical for the operation and maintanence of network systems.

These are services that typically run on the network server or home router.

Some of the most important ones include:


**DNS (Domain Name System)**


- Converts human-readable addresses into IP addresses and vice-versa.
- Distributed service. Many thousands of DNS servers are running around the world 24/7. Multiple servers balance the load.
- Specific servers manage specific websites and geographical areas.
- Usually managed by ISP or organisation.


**DHCP (Dynamic Host Configuration Protocol)**


-  Automatically configures IP settings on host devices so everything doesn't have to be manually setup every time.
- Runs on most home routers.
- Assigns host IPs from a pre-configured pool.
- Enterprise DHCP has redundancy built in (multiple servers) so it never falls over and typically runs on the company central servers.

**File Share**


- Some system of centralized storage of files and resources.
- Usually a standard protocol like *SMB (Server Message Block)* on Windows or *AFP (Apple Filing Protocol)* on MacOS.
- The actual protocol is usually hidden in the background behind front-end GUI.

**Print Server**


- A service that allows printer connection, use and management.
- Sometimes runs on a central server, sometimes on the printer itself if it has a built-in network card and service software.
- Standard printing protocols include:
- SMB (Server Message Block)
- IPP (Internet Printing Protocol)
- LPD (Line Printer Daemon)

**Mail Server**


- Sends mail and stores incoming mail.
- One of the most important services. Should never go down.
- Often cloud-based and managed by ISP or locally managed by enterprise IT dept.


**Syslog**


- Syslog is a protocol that allows diverse system log files from many locations to be consolidated in one database.
- Typically integrated in a SIEM (Security Information & Event Manager).
- Logs need to be kept for many years sometimes and large enterprises may generate huge volumes of log files.
- Large storage space is needed - sometimes hundreds of TB or PB.

**Web Server**


- Handles browser requests.
- Uses standard web protocols like HTTP/HTTPS
- Websites are built with standard markup languages like HTML so everything works.
- Web pages are stored on the server and downloaded to the browser.
- Sometimes the browser will deliver a cached version.

**Authenication Server**


- Sometimes called *AAA* server *(Authentication, Authorization, Accounting)*.
- Centralised database to manage logins and resource access.
- Almost always exists in enterprise systems.
- Usually features redundancy. Critical service.

**Database Servers**


- Stores and manages information in database tables similar to a spreadsheet.
- Tables that link to or reference each other are *relational databases*.
- Standard language for manipulating databases is *SQL*.
- Microsoft SQL Server, MySQL, etc.

**NTP (Network Time Protocol) Servers**


- Everything in a network needs to run off the same time and clock.
- Important for encryption, logins, backups and syncing, log timestamps, user schedules, etc.
- NTP server responds to time requests and references a central clock.
- NTP client makes requests for time sync updates, often daily.

**Spam Gateways**


- Analyses and filters incoming emails for spam at the firewall level.
- Can be cloud-based or on-site.


**All-in-one-security appliance**


Sometimes called a:
- Next-gen firewall.
- UTM (Unified Threat Management).
- Web security gateway.

A single device between the network and the internet that manages things such as:
- URL filter
- Malware inspection
- Spam filter
- Routers & Switches
- Firewalls
- Bandwidth shaping
- VPN functionality

**Load Balancer**


- Service that distributes load between servers.
- Web servers or database servers will be connected to a load balancer that managages their rotation.
- Outages in a single server won't crash operations.
- Fast and invisible to users.

**Proxy Server**


- Middle-man server that receives and passes on client requests to the real server.
- Used for security, content filtering, access control, caching, etc.
- Usually invisible to user.

**SCADA/ICS (Supervisory Control and Data Acquisition System) / (Industrial Control System)**



- Systems management service for industrial systems like power plants and factories.
- Provides real-time telemetry and control.
- Usually completely segmented network for security. Must physically access the system in person or remotely access through very strict and secure means.

**Legacy Systems and Embedded Systems**


- These are old services that have been running sometimes for decades.
- They may perform vital tasks but have never needed to have been updated.
- Embedded systems are purpose built, low maintanence and mostly invisible systems that you don't directly interact with typically. They run in the background until you have a problem with it you need to address.

**IoT (Internet of Things)**


- All kinds of devices that communicate over the network like smart home devices, fridges, etc.
- Manufacturers might be good at making appliances, but not so good at stable network technology or security.
- Can be useful to segment IoT device networks.