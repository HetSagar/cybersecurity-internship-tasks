# Task 1 - Basic Network Scanning with Nmap

## Objective

The objective of this task was to perform a network scan using Nmap to identify open ports and services running on a target machine.

## Tool Used

* Nmap

## Commands Executed

### Basic Scan

```bash
nmap <target-ip>
```

### Service Detection Scan

```bash
nmap -sV <target-ip>
```

## Findings

The scan identified active ports and services running on the target system.

### Open Ports

| Port                  | Protocol | Service | Description |
| --------------------- | -------- | ------- | ----------- |
| Add your results here |          |         |             |

## Significance of Open Ports

Explain each discovered port and its purpose.

Example:

* Port 135/TCP: Microsoft RPC service.
* Port 445/TCP: SMB file sharing service.
* Port 3389/TCP: Remote Desktop Protocol.

## Conclusion

Nmap successfully identified open ports and services on the target machine. Network scanning helps administrators understand exposed services and improve security posture.
