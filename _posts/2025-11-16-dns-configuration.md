---
layout: post
title: "DNS Configuration"
date: 2025-11-16 12:00:00 +1000
categories: networking
---
**DNS (Domain Name System)**


DNS is a critical service that resolves human-readable names like *www.google.com* to machine-readable values like an IP address of *103.86.96.100*, and vice-versa.

It essentially just matches names to more specific values a network can use.

It typically uses ports:
- udp/**53**
- tcp/**53**

It is a distributed database:
- Service is distributed among thousands of servers around the world.
- 13 root server clusters consisting of over 1000 servers.
- Hundreds of gTLDs (generic Top Level Domains) like .com .org. .net
- Over 275 ccTLDs (country code Top Level Domains) like .au .uk .fr

**DNS Structure**


DNS has a hierarchical tree structure.
- (ROOT). -> (TLDs).com -> (SECOND LEVEL DOMAIN)example.com -> (SUBDOMAIN)dev.example.com -> (HOSTNAME)www.dev.example.com
- An FQDN (Fully Qualified Domain Name) has this full hierarchy and is able to be associated with an IP address and other records.

To resolve an IP address, a client query flows as such:
- Browser might already have record cached and return the IP.
- Otherwise, goes to recursive DNS server perhaps managed by ISP or Cloudflare. Might return cached non-authoritative record if it's within TTL rules.
- Otherwise, asks ROOT server cluster (.) which then points to the server managing TLDs and ccTLDS.
- TLD server provides or points to server managing SECOND-LEVEL DOMAIN, SUBDOMAIN and usually HOSTNAME.
- Once the Fully Qualified Domain Name (FQDN) has been identified, the requested DNS records can be accessed and sent to the client.



**DNS Lookup**


In PowerShell (Windows) the *nslookup* command can be used to query a DNS database from the terminal.
- nslookup - interactive
- nslookup example.com - requests the associated IP addresses with that domain.
- nslookup 8.8.8.8 - reverse, requests the domain associated with the IP
- nslookup -type=mx example.com - requests a specific record type, in this case MX is the mail exchange record.

In Linux or Mac, the *dig* command is typically used, which has a bit more functionality than *nslookup*.

**DNS Records**


DNS records are pieces of data that define how a domain behaves. It tells querying servers where to find services and how to reach them, resolves IP/domain addresses, how long clients should cache information, etc.

There are over 30 record types.

These records can sit in a plain-text file, or more commonly now, the record configurations are stored in a back-end database operated by a 3rd party provider like Google DNS or Cloudflare, and the settings can be accessed through an API/web GUI.

Incorrectly editing or configuring records can break your whole DNS setup so it's best to backup before changing anything and to test everything.

Record text format typically goes: (NAME) (TTL) (CLASS) (TYPE) (RDATA/VALUE)

- (NAME) Human-readable value
- (TTL) Time To Live, How long clients/servers should cache the info in minutes
- (CLASS) Type class, only IN (Internet) is really used now.
- (TYPE) Record type e.g. AAAA, MX, etc.
- (VALUE) The record data value e.g. IP address for A record.

- At least TYPE and VALUE must be present.
- If name is missing, it might inherit from previous entry.
- If TTL is missing, it will inherit globally defined TTL by default.
- If CLASS is missing, it will assume IN by default.

Some of the most important records to be familiar with are:

**Address - A/AAAA**


- Defines the IP address of a host (host = device or service)
- **A** defines IPv4 addresses
- **AAAA** defines IPv6 addresses
- e.g. relto.com IN A 192.168.50.90

**Canonical Name - CNAME**


- Allows multiple names or aliases to point to one server location.
For example:
- ftp IN CNAME mail.example.com
- chat IN CNAME mail.example.com
Above, if a client references ftp.example.com or chat.example.com it will point both to the same mail.example.com server.

**Mail Exchanger - MX**


- Defines what server handles email for a domain.
- If a client asks a DNS server - "Where do I send mail for this domain: relto.example.com?" It references the MX record.
- The mail server domain is then queried again for the actual IP address.
- E.g. if your domain's mail was handled by Google Workspace, the MX record might look like: IN MX ASPMX.L.GOOGLE.COM
- You can list multiple servers or providers with different priority: mail1.example.com, mail2.example.com

**Text record - TXT**


- DNS records that store human-readable text.
- Stores useful information we would like other people or services to access.
- Can be used for storing verification keys, spam filter settings, etc.
- e.g. command query *nslookup -type=txt relto.com txt* might return: *relto.com text= "stripe-verification=4lkhfd873hdh38dsjhf93"*

**DKIM (Domain Keys Identified Mail) TXT record**
- Used to digitally sign a domain's outgoing mail.
- Public key is in the DKIM TXT record on the DNS server.
- Email server signs outgoing mail with a private encryption key.
- Receiving mail server fetches the public key from the DNS server and uses it to mathematically decrypt and compare the signatures to verify the email really was sent from the offical email server.
- TXT record looks something a bit like like: "v=DKIM ;t=s;p=FDlkhfdFKdlkfjdfDFKLJDFKLjFhDKFJhdfKDFJh/dsDFJhdj"


**SPF (Sender Policy Framework) TXT record**
- SPF protocol is a txt list of all servers authorised to send mail from a domain.
- Prevents mail spoofing
- Mail servers perform a check to see if incoming mail is from an authorised host on the SPF list.
- Looks something like IN TXT "v=spf1 include:mailgun.org ~all"
- If you receive mail from a host that isn't on the list, it's likely an unassociated spoof.

**DMARC (Domain-based Message Authentication, Reporting and Conformance) TXT record**
- DMARC is a policy txt record that tells an external mail server what it should do if it fails to validate mail from a domain with SPF or DKIM checks.
- Can tell the server to accept it, reject it or send it to spam and let the user decide.
- Compliance reports can be generated and sent to the originating mail domain admin.
- A txt record might look a bit like: "v=DMARC1;p=none;sp=quarantine; pct=100;rua=mailto:dmarcreports@example.com;" -  this would tell the server to quarantine unvalidated mail in user's spam and send a report to the admin.





