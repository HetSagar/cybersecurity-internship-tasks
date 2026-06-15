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

### Findings

* DNS packets were used to resolve domain names.
* TCP packets established and maintained network connections.
* HTTPS traffic was encrypted, protecting transmitted data.

## Security Observations

* Most web traffic was encrypted using HTTPS.
* DNS requests revealed domain lookups performed during browsing.
* Network monitoring tools can help identify suspicious activity and troubleshoot connectivity issues.

## Conclusion

Wireshark successfully captured and analyzed network traffic. Packet analysis provides valuable insight into network communications and helps security professionals identify potential issues and threats.
