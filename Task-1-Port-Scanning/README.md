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
**ipconfig**
Identify your IPv4 address and network range (for example: `192.168.1.0`).

### 2. Perform a TCP SYN Scan

Run the following command:
**nmap -sS 192.168.1.0**

To save the results:
**nmap -sS 192.168.1.0 -oN scan.txt**

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

# Research on Common Services Running on Open Ports

The Nmap scan identified the following open ports on the target system:

| Port    | Service                                 | Description                                                                               |
| ------- | --------------------------------------- | ----------------------------------------------------------------------------------------- |
| **135** | MSRPC (Microsoft Remote Procedure Call) | Used by Windows to enable communication between applications and network services.        |
| **139** | NetBIOS Session Service                 | Used for file and printer sharing on Windows networks using NetBIOS.                      |
| **445** | SMB (Microsoft-DS)                      | Used for Windows file sharing, printer sharing, and other network communication services. |

# Potential Security Risks

Open ports can expose a system to cyber attacks if they are not properly secured.
* **Port 135 (MSRPC):**
  * May allow attackers to gather information about the system.
  * Can be targeted if Windows vulnerabilities are not patched.

* **Port 139 (NetBIOS):**
  * May expose shared files and printers.
  * Weak or misconfigured file sharing can lead to unauthorized access.

* **Port 445 (SMB):**
  * Frequently targeted by malware and ransomware attacks.
  * Vulnerable systems may be exploited if Windows security updates are missing.

**Overall Risk:**
Keeping unnecessary ports open increases the attack surface and provides more opportunities for attackers to access the system.

# Recommendations

* Close unused or unnecessary ports.
* Enable and properly configure Windows Firewall.
* Keep Windows and installed software up to date.
* Disable file and printer sharing if it is not required.
* Use strong passwords and allow access only to trusted users and devices.

## Conclusion

The Nmap scan successfully identified the active hosts and open ports on the local network. Understanding the services running on these ports helps identify potential security risks and improve the overall security of the system by following best security practices.

## Author
**Jajwal Kumar**
Cyber Security Internship – Elevate Labs

