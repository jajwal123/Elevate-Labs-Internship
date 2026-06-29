# Task 1: Scan Your Local Network for Open Ports

## Objective
The objective of this task is to discover open ports on devices in a local network using Nmap and understand basic network reconnaissance.

## Tools Used
- Nmap
- Windows Command Prompt
- GitHub

## Steps Performed

### 1. Find the Local IP Address
Open Command Prompt and run:

```bash
ipconfig
```

Identify your IPv4 address and network range (for example: `192.168.1.0`).

### 2. Perform a TCP SYN Scan

Run the following command:

```bash
nmap -sS 192.168.1.0
```

To save the results:

```bash
nmap -sS 192.168.1.0 -oN scan.txt
```

## Results
- Successfully scanned the local network.
- Identified active hosts.
- Detected open ports and running services.
- Saved the scan results to `scan.txt`.

## Findings
- Open ports indicate services that are accepting network connections.
- Port scanning helps identify active devices and exposed services.
- Understanding open ports is important for improving network security.

## Conclusion
This task provided hands-on experience with Nmap and demonstrated how to identify open ports, active hosts, and network services within a local network.

## Files Included
- `README.md`
- 'Interview Question'
- `scan_results.txt`
- `screenshots/ipaddress.png`
- `screenshots/nmap_scan.png`

## Author
**Jajwal Kumar**

Cyber Security Internship – Elevate Labs
