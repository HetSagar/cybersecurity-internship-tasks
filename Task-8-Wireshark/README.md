# Task 8 - Network Traffic Analysis with Wireshark

## Objective

The objective of this task was to capture and analyze network traffic using Wireshark.

## Tool Used
* Wireshark

## Procedure

1. Installed and launched Wireshark.
2. Selected the active network interface.
3. Captured network traffic while browsing websites.
4. Applied protocol filters to analyze traffic.
5. Examined packet details and protocol information.

## Traffic Analysis

The packet capture contained network communication generated during normal web browsing activity.

### Protocols Observed

* TCP
* DNS
* HTTPS

## Traffic Analysis Findings

The captured traffic primarily consisted of DNS queries and responses generated during normal web browsing activity.

### Protocols Identified

* DNS (Domain Name System)
* UDP (User Datagram Protocol)
* IPv6
* Ethernet II

### Observations

Several DNS queries were observed for domains including:

* [www.youtube.com](http://www.youtube.com)
* play.google.com
* charusat.edu.in
* ogads-pa.clients6.google.com

The packets demonstrated the DNS resolution process in which domain names are translated into IP addresses before network communication occurs.

### Packet Example

One captured packet showed:

* Source Port: 61891
* Destination Port: 53
* Protocol: DNS

This indicates that the client device initiated a DNS request to a DNS server to resolve a domain name.

### Security Considerations

* DNS traffic can reveal websites and services accessed by users.
* Monitoring DNS activity helps detect malicious domains and suspicious communications.
* Encrypted web traffic (HTTPS) protects data transmission after DNS resolution occurs.


## Security Observations

* Most web traffic was encrypted using HTTPS.
* DNS requests revealed domain lookups performed during browsing.
* Network monitoring tools can help identify suspicious activity and troubleshoot connectivity issues.

## Conclusion

Wireshark successfully captured and analyzed network traffic. Packet analysis provides valuable insight into network communications and helps security professionals identify potential issues and threats.
