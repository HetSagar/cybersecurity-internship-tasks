# Task 1 - Basic Network Scanning with Nmap

## Objective

The objective of this task was to perform a network scan using Nmap to identify open ports and services running on a target machine.

## Tool Used

* Nmap 7.98

## Commands Executed

### Basic Scan

```bash
nmap 192.168.22.165
```

## Scan Results

```
Starting Nmap 7.98 at 2026-06-15

Nmap scan report for 192.168.22.165
Host is up (0.00018s latency).

Not shown: 997 closed tcp ports (reset)

PORT    STATE SERVICE
135/tcp open  msrpc
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds
```

## Open Ports and Services

| Port    | Service      | Description                                                                                               |
| ------- | ------------ | --------------------------------------------------------------------------------------------------------- |
| 135/TCP | MSRPC        | Microsoft Remote Procedure Call service used for communication between Windows applications and services. |
| 139/TCP | NetBIOS-SSN  | NetBIOS Session Service used for file and printer sharing on local networks.                              |
| 445/TCP | Microsoft-DS | SMB (Server Message Block) protocol used for file sharing, printer sharing, and network communication.    |

## Significance of Open Ports

### Port 135 (MSRPC)

This port is used by Windows for Remote Procedure Calls (RPC). It enables communication between client and server applications and is essential for many Windows services.

### Port 139 (NetBIOS-SSN)

This port supports NetBIOS sessions and is commonly used for network file and printer sharing. It is primarily found in Windows environments.

### Port 445 (Microsoft-DS)

This port is associated with the SMB protocol. SMB allows systems to share files, folders, and printers over a network. Because SMB has historically been targeted by malware and ransomware, it should only be exposed when necessary.

## Security Considerations

* Disable unnecessary file-sharing services if not required.
* Restrict SMB access through firewall rules.
* Keep Windows systems updated with the latest security patches.
* Monitor network services regularly using security assessment tools.

## Service Detection Results

| Port    | State | Service      | Version Information                       |
| ------- | ----- | ------------ | ----------------------------------------- |
| 135/TCP | Open  | MSRPC        | Microsoft Windows RPC                     |
| 139/TCP | Open  | NetBIOS-SSN  | Microsoft Windows NetBIOS Session Service |
| 445/TCP | Open  | Microsoft-DS | SMB/File Sharing Service                  |
| OS Info | -     | -            | Microsoft Windows                         |

## Analysis

The Nmap service detection scan identified three open ports commonly associated with Windows networking services.

### Port 135 – MSRPC

Microsoft Remote Procedure Call (RPC) enables communication between Windows applications and services. It is required for many administrative functions.

### Port 139 – NetBIOS Session Service

NetBIOS provides network communication and supports file and printer sharing within Windows environments.

### Port 445 – Microsoft Directory Services (SMB)

Port 445 is used by the SMB protocol for file and printer sharing. Because SMB services have historically been targeted by malware and ransomware attacks, organizations should restrict access and keep systems patched.

## Security Recommendations

1. Disable unused file-sharing services.
2. Restrict SMB access through firewall rules.
3. Regularly apply Windows security updates.
4. Conduct periodic network scans to identify exposed services.
5. Monitor suspicious activity on network-facing ports.


## Conclusion

The Nmap scan successfully identified three open ports running on the target Windows machine. These ports are associated with core Windows networking and file-sharing services. Regular network scanning helps identify exposed services and supports proactive security management.
